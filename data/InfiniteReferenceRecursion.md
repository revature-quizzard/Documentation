## Infinite Reference Recursion due to circular / bi-directional relations
We have found that having a circular or bi-directional relation causes numerous problems. We can't anticipate a need for this sort of 
setup, and during our testing we found the best thing to do is avoid this at all costs. Even with the @JsonIgnoreProperties annotation properly set up,
some functions still use HashCode and toString which would need to be re-tooled to not infinitely recurse. Because this functionality is buried deep 
under the hood in many places we decided to just not do it.


### Avoid this:
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
    
    @OneToMany
    private Set<Egg> eggs;
  }
```

Instead only include the reference where necessary, referring to the PK of the referenced object from the foreign key field.
