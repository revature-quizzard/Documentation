# Infinite Reference Recursion due to circular / bi-directional relations
We have found that having a circular or bi-directional relation causes numerous problems. We can't anticipate a need for this sort of 
setup, and during our testing we found the best thing to do is avoid this at all costs. Even with the @JsonIgnoreProperties annotation properly set up,
some functions still use HashCode and toString which would need to be re-tooled to not infinitely recurse. Because this functionality is buried deep 
under the hood in many places we decided to just not do it.
## Many-to-One and One-to-one
In these relations we only need the reference on the side that contains the foreign key referencing the primary key of the other table, in accordance with the ERD.
### Correct way:
```
@Entity
public class Egg {
  private int id;
  
  @ManyToOne
  private Basket basket;

}
```

```
@Entity
  public class Basket {
    private int id;
  }
```

Instead only include the reference where necessary, referring to the PK of the referenced object from the foreign key field.

## Many-to-many
The same goes for many-to-many relations where there would be a junction table. Only the "owner" side needs the reference. That is, the side that should be serialized to include
the other side. The owner side needs a @JoinTable annotation. The owned side does not need a collection field or any reference to the owner side.

### Correct way:
```
public class Students {

  @Id
  @Column(name = "student_id")
  private int id;
  
  @ManyToMany
  @JoinTable(
        name = "students_courses",
        joinColumns = { @JoinColumn(name = "student_id")},
        inverseJoinColumns = { @JoinColumn(name = "course_id") }
    )
  private Set<Courses> courses;
}
```
```
//No need for a backward reference!
public class Courses {

  @Id
  @Column(name = "course_id")
  private int id;
  
  private String courseName;
}

```
