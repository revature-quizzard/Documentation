# Example CognitoUser Object

The following is an example of the CognitoUser object that is sent in the response when a user logs in, 
for better understanding what we recieve from Cognito and determining how we wish to handle it.

```
{
    "username": "example_user",
    "pool": {
        "userPoolId": "user_pool_id",
        "clientId": "client_id",
        "client": {
            "endpoint": "https://cognito-idp.us-east-2.amazonaws.com/",
            "fetchOptions": {}
        },
        "advancedSecurityDataCollectionFlag": true,
        "storage": {
            "CognitoIdentityServiceProvider.client_id.example_user.accessToken": "eyJraWQiOiI0SlZLQjF2VVlNa3hxc1ZCWjh2MUUzMmt2Mkw0XC95NEdiZzVpWmE1ZURBOD0iLCJhbGciOiJSUzI1NiJ9.eyJvcmlnaW5fanRpIjoiYWUxMWNkODQtZjcxOC00NWU1LTg3MjItOGYyOTRmZGY2ZGE2Iiwic3ViIjoiNWIwMDA1OWUtYTg0Yy00Y2JmLWIyZWUtOTM1Zjc3ODUyMzYwIiwiZXZlbnRfaWQiOiI4ZTBkMDVkMi0zZTI1LTRkOWUtOTkyNy1jMWQyNWJjY2VmYjEiLCJ0b2tlbl91c2UiOiJhY2Nlc3MiLCJzY29wZSI6ImF3cy5jb2duaXRvLnNpZ25pbi51c2VyLmFkbWluIiwiYXV0aF90aW1lIjoxNjMyNDU5NTQxLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9tTkkySmc0blUiLCJleHAiOjE2MzI0NjMxNDEsImlhdCI6MTYzMjQ1OTU0MSwianRpIjoiNDdlZDNlZjgtZWVmZi00MTBmLTk2ZDctMWVmNDcxNTEyOTY4IiwiY2xpZW50X2lkIjoiajM5MWk5czVtbjJnaDY4ZzQzYm1nYTEwayIsInVzZXJuYW1lIjoiY3NtY2RvbiJ9.oWDwC25shSC9vVB1X4h7QpFx9osOY5BDgvrw524J80uhqqlER6Csmgu2c_nxB-QjVhkHhlhOCJhHeVHAj9oVTJ5MIkZOQldaQZWT9y5lJbpdqNsWF8OKzhO2O1rhm3TrQmEHYt_ewlCn1A4XrZR4pLI3-k-aqon8XCo7xMBRwaMot4ofzf_jaNcdbf3i3WDHRRunPJP6nrA3HODBgQSxwPpG9iDz8Gqr_KM0tglkmyMWG_mMHiyJfI6TI9pp0FCgjNmAZskXOOunppMtBS-NQb2ifU0VnkqcaB53Wc95ngjvS9eROM3Stm7SSU5RQnWM75tbk7LfWTmnaPt_pImn3w",
            "CognitoIdentityServiceProvider.client_id.example_user.refreshToken": "eyJjdHkiOiJKV1QiLCJlbmMiOiJBMjU2R0NNIiwiYWxnIjoiUlNBLU9BRVAifQ.mjVLXTNUqrbXDww6zsm0S9JG4A3Vmf698k0UJRjnPfnZ-bjKrTN7wPYVvyXsKxUZaE9Idclz1C3yIsMVGwdo9aV2cQ73wR2ISeB8FH1DfNtgIayp-glVkCfv-h18yp7sZ60bLC4djspUP_B87D2TIHsKgrfGL2D_YMdBT_pmwAmFv6wzl0g84dWGgCuVMuJd41806XrFqqGWxGTEgVylr1sKEfVMr9W_Q8DrrLprCHKs2AgU6V-n31NrsLd0rt126gYh9Aym0J_YRpHi_us3t5AMj9Y6-3Do_ArgbKYt7qDKiCBB7IPPzvcS5GS7sSaK0u-TAZjHaZHQxvRJImOm5w.oERNZflO2vkHQZMD.pu-XH0hGYHX07E3j8aNOS0CM3JvQw9Ygs4-c5UfskvNFW1Pr8Kq8YY67MXYKm1skghmCnA3w15Z_gBzE8qexzdvvBNMGv_3frjqPpc0lCDtVrP99dqlYM9aLrby-xTnszTyvpCTIvKZ07asccvjxCCH_VXZ25c0U3KOTjmN1X0IjJATp5yxtrudJYoABmO2CJ8rqLjFkBij6PrDIgT-amRYGzxtTAgxU5cLmW4OM0IhpMCELpFm7f7m9-XOCaghO0R_EgM7xwYltggLRfsKTucOdHNrUjlT0TJDjVdCG7GXu1vrfyo_11sqdRyQJIw3WMaiPfQcx6AHo63mw28RMm6-5XKDvQDI9_iwW8FA0-vKpjZolWpYvhb-A9ZXzgKLgzdvy23ab6kDQilCgdyetnhiViTN86l2utlS8BnlPy0A0OZTbPwC_tSfR89iuT8O63eJc0_TIaV6EPrrjmZuzRNI0SgVczrm_DXZEEbLD8OAfMvN29qBsc3GHuU3CmimRQL4qXHXPiRZpXialpNGKFZW5ELSRE4PwxemR922Q5xqhfbiZpQ1kJ9tBU2sWCi0TRbvKtedsvTsZ0Cy6MKlfosmUR8lG6gVaSHZ_bJwEALBfI49MAinjJBct5zURWdFAgCQtxpr5yjnixdWmbvWX0FzSMJfkoDVp-b18MYj4hC8MjydxR3OD3Tfapcy9n5HLa1nPHp3dRy71oJHU6RfBqKm3RTYFUL48vn-rha6fegtyULlFezieiRp7_Bh5qCo70hnDKmqFJZodQjHwqdQ4jHKA_ToO0qKgNKDFKGURAp3yEkNbB8H1EVfjkX2BUd_v1Gj2PpXHvK0kq2Wc1LiZ9cqNnmc4_XmWc3odB2Qqh2-2FGJQMzsbjCvcSRNj55KQql71mVhP_0KqWIopomgXtYud7s8vdtsx0C8kWi_JScUeUApFUBI-jZznQ_uWFcmfT68wQEXIkl1HO6djxWaPjG3qWrVlMCZ5I4H1DybIguSfKTKhx3I0fTM74wbwUa9AhEDr8msRimoE0X_aSkOKCKAgCuajoOrSoE_Rj26wf0FtdoqCD0XeLugeoC9c6nv-PV-xCCt35MNCx1l7MJAqV94VhafT_Ssx33wzhLbOdWdvLYSRYyEPwquyUzRD3EYco4axyiTOK66mf1IOkpVikV2mpxsTI_ACCmbnpjfrWBiv_f-7KDMvthnv3Sx7CUTBBAbxWscFx7nCnO2tpXID237XabssdqWffPkhhUP-3oRZj90WKlx60JgREFlb-Az7sJQ0.Qrs6BO2IcsaZb6UgGG1HXA",
            "amplify-signin-with-hostedUI": "false",
            "CognitoIdentityServiceProvider.client_id.example_user.idToken": "eyJraWQiOiJlTW5iMG9Wd29hQ1wvR1lzcVZSOFN3SmpvbTlXSVhKa3dlQjhEcE5ISGc2cz0iLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiI1YjAwMDU5ZS1hODRjLTRjYmYtYjJlZS05MzVmNzc4NTIzNjAiLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLnVzLWVhc3QtMi5hbWF6b25hd3MuY29tXC91cy1lYXN0LTJfbU5JMkpnNG5VIiwiY29nbml0bzp1c2VybmFtZSI6ImNzbWNkb24iLCJvcmlnaW5fanRpIjoiYWUxMWNkODQtZjcxOC00NWU1LTg3MjItOGYyOTRmZGY2ZGE2IiwiYXVkIjoiajM5MWk5czVtbjJnaDY4ZzQzYm1nYTEwayIsImV2ZW50X2lkIjoiOGUwZDA1ZDItM2UyNS00ZDllLTk5MjctYzFkMjViY2NlZmIxIiwidG9rZW5fdXNlIjoiaWQiLCJhdXRoX3RpbWUiOjE2MzI0NTk1NDEsIm5hbWUiOiJDb2R5IE1jRG9uYWxkIiwiZXhwIjoxNjMyNDYzMTQxLCJpYXQiOjE2MzI0NTk1NDEsImp0aSI6IjVkOWI2ZTU5LWI1NDgtNGM4Yy05MjcxLTUxZTY1NzNkOTAzYiIsImVtYWlsIjoiY29keS5tY2RvbmFsZEByZXZhdHVyZS5uZXQifQ.3Jpjc-gkNez14h7F4GvkI3vcbV0Nx39yt9LrqYTREBpsw4G01xY1N-S33q75TGdTgfCvUne5yzH2NEcj55tt-oLjBqqtDhNFcVSKstHqI0LCwcTHLs9qArwhq2nxgPff7n3sHQOMMU6fHEr3bpMnfWvRozRxqkeFqLwwx4biK0_OBj_Y5P0kRIZCaq_g2OF850NkuMre-QYDIkFLkh3X15_DqyTJ_Y5Zhb7oJZfYtfZHTpW3KqU6-88pCFTwaLt5TYZAimbUGZhHl1yQpjPDM-EkTq8A_d8U6Pn0IlyXvJ_7LvtqC9XSF9idiaWhDGlDrwcELTZ6-Do7asp0LeOwNw",
            "CognitoIdentityServiceProvider.client_id.LastAuthUser": "example_user",
            "CognitoIdentityServiceProvider.client_id.example_user.clockDrift": "-1",
            "CognitoIdentityServiceProvider.client_id.example_user.userData": "{\"UserAttributes\":[{\"Name\":\"sub\",\"Value\":\"example_user_id\"},{\"Name\":\"email_verified\",\"Value\":\"true\"},{\"Name\":\"name\",\"Value\":\"Test User\"},{\"Name\":\"email\",\"Value\":\"example.email@test.net\"}],\"Username\":\"example_user\"}"
        }
    },
    "Session": null,
    "client": {
        "endpoint": "https://cognito-idp.us-east-2.amazonaws.com/",
        "fetchOptions": {}
    },
    "signInUserSession": {
        "idToken": {
            "jwtToken": "eyJraWQiOiJlTW5iMG9Wd29hQ1wvR1lzcVZSOFN3SmpvbTlXSVhKa3dlQjhEcE5ISGc2cz0iLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiI1YjAwMDU5ZS1hODRjLTRjYmYtYjJlZS05MzVmNzc4NTIzNjAiLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLnVzLWVhc3QtMi5hbWF6b25hd3MuY29tXC91cy1lYXN0LTJfbU5JMkpnNG5VIiwiY29nbml0bzp1c2VybmFtZSI6ImNzbWNkb24iLCJvcmlnaW5fanRpIjoiYWUxMWNkODQtZjcxOC00NWU1LTg3MjItOGYyOTRmZGY2ZGE2IiwiYXVkIjoiajM5MWk5czVtbjJnaDY4ZzQzYm1nYTEwayIsImV2ZW50X2lkIjoiOGUwZDA1ZDItM2UyNS00ZDllLTk5MjctYzFkMjViY2NlZmIxIiwidG9rZW5fdXNlIjoiaWQiLCJhdXRoX3RpbWUiOjE2MzI0NTk1NDEsIm5hbWUiOiJDb2R5IE1jRG9uYWxkIiwiZXhwIjoxNjMyNDYzMTQxLCJpYXQiOjE2MzI0NTk1NDEsImp0aSI6IjVkOWI2ZTU5LWI1NDgtNGM4Yy05MjcxLTUxZTY1NzNkOTAzYiIsImVtYWlsIjoiY29keS5tY2RvbmFsZEByZXZhdHVyZS5uZXQifQ.3Jpjc-gkNez14h7F4GvkI3vcbV0Nx39yt9LrqYTREBpsw4G01xY1N-S33q75TGdTgfCvUne5yzH2NEcj55tt-oLjBqqtDhNFcVSKstHqI0LCwcTHLs9qArwhq2nxgPff7n3sHQOMMU6fHEr3bpMnfWvRozRxqkeFqLwwx4biK0_OBj_Y5P0kRIZCaq_g2OF850NkuMre-QYDIkFLkh3X15_DqyTJ_Y5Zhb7oJZfYtfZHTpW3KqU6-88pCFTwaLt5TYZAimbUGZhHl1yQpjPDM-EkTq8A_d8U6Pn0IlyXvJ_7LvtqC9XSF9idiaWhDGlDrwcELTZ6-Do7asp0LeOwNw",
            "payload": {
                "sub": "example_user_id",
                "email_verified": true,
                "iss": "https://cognito-idp.us-east-2.amazonaws.com/user_pool_id",
                "cognito:username": "example_user",
                "origin_jti": "ae11cd84-f718-45e5-8722-8f294fdf6da6",
                "aud": "client_id",
                "event_id": "8e0d05d2-3e25-4d9e-9927-c1d25bccefb1",
                "token_use": "id",
                "auth_time": 1632459541,
                "name": "Test User",
                "exp": 1632463141,
                "iat": 1632459541,
                "jti": "5d9b6e59-b548-4c8c-9271-51e6573d903b",
                "email": "example.email@test.net"
            }
        },
        "refreshToken": {
            "token": "eyJjdHkiOiJKV1QiLCJlbmMiOiJBMjU2R0NNIiwiYWxnIjoiUlNBLU9BRVAifQ.mjVLXTNUqrbXDww6zsm0S9JG4A3Vmf698k0UJRjnPfnZ-bjKrTN7wPYVvyXsKxUZaE9Idclz1C3yIsMVGwdo9aV2cQ73wR2ISeB8FH1DfNtgIayp-glVkCfv-h18yp7sZ60bLC4djspUP_B87D2TIHsKgrfGL2D_YMdBT_pmwAmFv6wzl0g84dWGgCuVMuJd41806XrFqqGWxGTEgVylr1sKEfVMr9W_Q8DrrLprCHKs2AgU6V-n31NrsLd0rt126gYh9Aym0J_YRpHi_us3t5AMj9Y6-3Do_ArgbKYt7qDKiCBB7IPPzvcS5GS7sSaK0u-TAZjHaZHQxvRJImOm5w.oERNZflO2vkHQZMD.pu-XH0hGYHX07E3j8aNOS0CM3JvQw9Ygs4-c5UfskvNFW1Pr8Kq8YY67MXYKm1skghmCnA3w15Z_gBzE8qexzdvvBNMGv_3frjqPpc0lCDtVrP99dqlYM9aLrby-xTnszTyvpCTIvKZ07asccvjxCCH_VXZ25c0U3KOTjmN1X0IjJATp5yxtrudJYoABmO2CJ8rqLjFkBij6PrDIgT-amRYGzxtTAgxU5cLmW4OM0IhpMCELpFm7f7m9-XOCaghO0R_EgM7xwYltggLRfsKTucOdHNrUjlT0TJDjVdCG7GXu1vrfyo_11sqdRyQJIw3WMaiPfQcx6AHo63mw28RMm6-5XKDvQDI9_iwW8FA0-vKpjZolWpYvhb-A9ZXzgKLgzdvy23ab6kDQilCgdyetnhiViTN86l2utlS8BnlPy0A0OZTbPwC_tSfR89iuT8O63eJc0_TIaV6EPrrjmZuzRNI0SgVczrm_DXZEEbLD8OAfMvN29qBsc3GHuU3CmimRQL4qXHXPiRZpXialpNGKFZW5ELSRE4PwxemR922Q5xqhfbiZpQ1kJ9tBU2sWCi0TRbvKtedsvTsZ0Cy6MKlfosmUR8lG6gVaSHZ_bJwEALBfI49MAinjJBct5zURWdFAgCQtxpr5yjnixdWmbvWX0FzSMJfkoDVp-b18MYj4hC8MjydxR3OD3Tfapcy9n5HLa1nPHp3dRy71oJHU6RfBqKm3RTYFUL48vn-rha6fegtyULlFezieiRp7_Bh5qCo70hnDKmqFJZodQjHwqdQ4jHKA_ToO0qKgNKDFKGURAp3yEkNbB8H1EVfjkX2BUd_v1Gj2PpXHvK0kq2Wc1LiZ9cqNnmc4_XmWc3odB2Qqh2-2FGJQMzsbjCvcSRNj55KQql71mVhP_0KqWIopomgXtYud7s8vdtsx0C8kWi_JScUeUApFUBI-jZznQ_uWFcmfT68wQEXIkl1HO6djxWaPjG3qWrVlMCZ5I4H1DybIguSfKTKhx3I0fTM74wbwUa9AhEDr8msRimoE0X_aSkOKCKAgCuajoOrSoE_Rj26wf0FtdoqCD0XeLugeoC9c6nv-PV-xCCt35MNCx1l7MJAqV94VhafT_Ssx33wzhLbOdWdvLYSRYyEPwquyUzRD3EYco4axyiTOK66mf1IOkpVikV2mpxsTI_ACCmbnpjfrWBiv_f-7KDMvthnv3Sx7CUTBBAbxWscFx7nCnO2tpXID237XabssdqWffPkhhUP-3oRZj90WKlx60JgREFlb-Az7sJQ0.Qrs6BO2IcsaZb6UgGG1HXA"
        },
        "accessToken": {
            "jwtToken": "eyJraWQiOiI0SlZLQjF2VVlNa3hxc1ZCWjh2MUUzMmt2Mkw0XC95NEdiZzVpWmE1ZURBOD0iLCJhbGciOiJSUzI1NiJ9.eyJvcmlnaW5fanRpIjoiYWUxMWNkODQtZjcxOC00NWU1LTg3MjItOGYyOTRmZGY2ZGE2Iiwic3ViIjoiNWIwMDA1OWUtYTg0Yy00Y2JmLWIyZWUtOTM1Zjc3ODUyMzYwIiwiZXZlbnRfaWQiOiI4ZTBkMDVkMi0zZTI1LTRkOWUtOTkyNy1jMWQyNWJjY2VmYjEiLCJ0b2tlbl91c2UiOiJhY2Nlc3MiLCJzY29wZSI6ImF3cy5jb2duaXRvLnNpZ25pbi51c2VyLmFkbWluIiwiYXV0aF90aW1lIjoxNjMyNDU5NTQxLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9tTkkySmc0blUiLCJleHAiOjE2MzI0NjMxNDEsImlhdCI6MTYzMjQ1OTU0MSwianRpIjoiNDdlZDNlZjgtZWVmZi00MTBmLTk2ZDctMWVmNDcxNTEyOTY4IiwiY2xpZW50X2lkIjoiajM5MWk5czVtbjJnaDY4ZzQzYm1nYTEwayIsInVzZXJuYW1lIjoiY3NtY2RvbiJ9.oWDwC25shSC9vVB1X4h7QpFx9osOY5BDgvrw524J80uhqqlER6Csmgu2c_nxB-QjVhkHhlhOCJhHeVHAj9oVTJ5MIkZOQldaQZWT9y5lJbpdqNsWF8OKzhO2O1rhm3TrQmEHYt_ewlCn1A4XrZR4pLI3-k-aqon8XCo7xMBRwaMot4ofzf_jaNcdbf3i3WDHRRunPJP6nrA3HODBgQSxwPpG9iDz8Gqr_KM0tglkmyMWG_mMHiyJfI6TI9pp0FCgjNmAZskXOOunppMtBS-NQb2ifU0VnkqcaB53Wc95ngjvS9eROM3Stm7SSU5RQnWM75tbk7LfWTmnaPt_pImn3w",
            "payload": {
                "origin_jti": "ae11cd84-f718-45e5-8722-8f294fdf6da6",
                "sub": "example_user_id",
                "event_id": "8e0d05d2-3e25-4d9e-9927-c1d25bccefb1",
                "token_use": "access",
                "scope": "aws.cognito.signin.user.admin",
                "auth_time": 1632459541,
                "iss": "https://cognito-idp.us-east-2.amazonaws.com/user_pool_id",
                "exp": 1632463141,
                "iat": 1632459541,
                "jti": "47ed3ef8-eeff-410f-96d7-1ef471512968",
                "client_id": "client_id",
                "username": "example_user"
            }
        },
        "clockDrift": -1
    },
    "authenticationFlowType": "USER_SRP_AUTH",
    "storage": {
        "CognitoIdentityServiceProvider.client_id.example_user.accessToken": "eyJraWQiOiI0SlZLQjF2VVlNa3hxc1ZCWjh2MUUzMmt2Mkw0XC95NEdiZzVpWmE1ZURBOD0iLCJhbGciOiJSUzI1NiJ9.eyJvcmlnaW5fanRpIjoiYWUxMWNkODQtZjcxOC00NWU1LTg3MjItOGYyOTRmZGY2ZGE2Iiwic3ViIjoiNWIwMDA1OWUtYTg0Yy00Y2JmLWIyZWUtOTM1Zjc3ODUyMzYwIiwiZXZlbnRfaWQiOiI4ZTBkMDVkMi0zZTI1LTRkOWUtOTkyNy1jMWQyNWJjY2VmYjEiLCJ0b2tlbl91c2UiOiJhY2Nlc3MiLCJzY29wZSI6ImF3cy5jb2duaXRvLnNpZ25pbi51c2VyLmFkbWluIiwiYXV0aF90aW1lIjoxNjMyNDU5NTQxLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9tTkkySmc0blUiLCJleHAiOjE2MzI0NjMxNDEsImlhdCI6MTYzMjQ1OTU0MSwianRpIjoiNDdlZDNlZjgtZWVmZi00MTBmLTk2ZDctMWVmNDcxNTEyOTY4IiwiY2xpZW50X2lkIjoiajM5MWk5czVtbjJnaDY4ZzQzYm1nYTEwayIsInVzZXJuYW1lIjoiY3NtY2RvbiJ9.oWDwC25shSC9vVB1X4h7QpFx9osOY5BDgvrw524J80uhqqlER6Csmgu2c_nxB-QjVhkHhlhOCJhHeVHAj9oVTJ5MIkZOQldaQZWT9y5lJbpdqNsWF8OKzhO2O1rhm3TrQmEHYt_ewlCn1A4XrZR4pLI3-k-aqon8XCo7xMBRwaMot4ofzf_jaNcdbf3i3WDHRRunPJP6nrA3HODBgQSxwPpG9iDz8Gqr_KM0tglkmyMWG_mMHiyJfI6TI9pp0FCgjNmAZskXOOunppMtBS-NQb2ifU0VnkqcaB53Wc95ngjvS9eROM3Stm7SSU5RQnWM75tbk7LfWTmnaPt_pImn3w",
        "CognitoIdentityServiceProvider.client_id.example_user.refreshToken": "eyJjdHkiOiJKV1QiLCJlbmMiOiJBMjU2R0NNIiwiYWxnIjoiUlNBLU9BRVAifQ.mjVLXTNUqrbXDww6zsm0S9JG4A3Vmf698k0UJRjnPfnZ-bjKrTN7wPYVvyXsKxUZaE9Idclz1C3yIsMVGwdo9aV2cQ73wR2ISeB8FH1DfNtgIayp-glVkCfv-h18yp7sZ60bLC4djspUP_B87D2TIHsKgrfGL2D_YMdBT_pmwAmFv6wzl0g84dWGgCuVMuJd41806XrFqqGWxGTEgVylr1sKEfVMr9W_Q8DrrLprCHKs2AgU6V-n31NrsLd0rt126gYh9Aym0J_YRpHi_us3t5AMj9Y6-3Do_ArgbKYt7qDKiCBB7IPPzvcS5GS7sSaK0u-TAZjHaZHQxvRJImOm5w.oERNZflO2vkHQZMD.pu-XH0hGYHX07E3j8aNOS0CM3JvQw9Ygs4-c5UfskvNFW1Pr8Kq8YY67MXYKm1skghmCnA3w15Z_gBzE8qexzdvvBNMGv_3frjqPpc0lCDtVrP99dqlYM9aLrby-xTnszTyvpCTIvKZ07asccvjxCCH_VXZ25c0U3KOTjmN1X0IjJATp5yxtrudJYoABmO2CJ8rqLjFkBij6PrDIgT-amRYGzxtTAgxU5cLmW4OM0IhpMCELpFm7f7m9-XOCaghO0R_EgM7xwYltggLRfsKTucOdHNrUjlT0TJDjVdCG7GXu1vrfyo_11sqdRyQJIw3WMaiPfQcx6AHo63mw28RMm6-5XKDvQDI9_iwW8FA0-vKpjZolWpYvhb-A9ZXzgKLgzdvy23ab6kDQilCgdyetnhiViTN86l2utlS8BnlPy0A0OZTbPwC_tSfR89iuT8O63eJc0_TIaV6EPrrjmZuzRNI0SgVczrm_DXZEEbLD8OAfMvN29qBsc3GHuU3CmimRQL4qXHXPiRZpXialpNGKFZW5ELSRE4PwxemR922Q5xqhfbiZpQ1kJ9tBU2sWCi0TRbvKtedsvTsZ0Cy6MKlfosmUR8lG6gVaSHZ_bJwEALBfI49MAinjJBct5zURWdFAgCQtxpr5yjnixdWmbvWX0FzSMJfkoDVp-b18MYj4hC8MjydxR3OD3Tfapcy9n5HLa1nPHp3dRy71oJHU6RfBqKm3RTYFUL48vn-rha6fegtyULlFezieiRp7_Bh5qCo70hnDKmqFJZodQjHwqdQ4jHKA_ToO0qKgNKDFKGURAp3yEkNbB8H1EVfjkX2BUd_v1Gj2PpXHvK0kq2Wc1LiZ9cqNnmc4_XmWc3odB2Qqh2-2FGJQMzsbjCvcSRNj55KQql71mVhP_0KqWIopomgXtYud7s8vdtsx0C8kWi_JScUeUApFUBI-jZznQ_uWFcmfT68wQEXIkl1HO6djxWaPjG3qWrVlMCZ5I4H1DybIguSfKTKhx3I0fTM74wbwUa9AhEDr8msRimoE0X_aSkOKCKAgCuajoOrSoE_Rj26wf0FtdoqCD0XeLugeoC9c6nv-PV-xCCt35MNCx1l7MJAqV94VhafT_Ssx33wzhLbOdWdvLYSRYyEPwquyUzRD3EYco4axyiTOK66mf1IOkpVikV2mpxsTI_ACCmbnpjfrWBiv_f-7KDMvthnv3Sx7CUTBBAbxWscFx7nCnO2tpXID237XabssdqWffPkhhUP-3oRZj90WKlx60JgREFlb-Az7sJQ0.Qrs6BO2IcsaZb6UgGG1HXA",
        "amplify-signin-with-hostedUI": "false",
        "CognitoIdentityServiceProvider.client_id.example_user.idToken": "eyJraWQiOiJlTW5iMG9Wd29hQ1wvR1lzcVZSOFN3SmpvbTlXSVhKa3dlQjhEcE5ISGc2cz0iLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiI1YjAwMDU5ZS1hODRjLTRjYmYtYjJlZS05MzVmNzc4NTIzNjAiLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLnVzLWVhc3QtMi5hbWF6b25hd3MuY29tXC91cy1lYXN0LTJfbU5JMkpnNG5VIiwiY29nbml0bzp1c2VybmFtZSI6ImNzbWNkb24iLCJvcmlnaW5fanRpIjoiYWUxMWNkODQtZjcxOC00NWU1LTg3MjItOGYyOTRmZGY2ZGE2IiwiYXVkIjoiajM5MWk5czVtbjJnaDY4ZzQzYm1nYTEwayIsImV2ZW50X2lkIjoiOGUwZDA1ZDItM2UyNS00ZDllLTk5MjctYzFkMjViY2NlZmIxIiwidG9rZW5fdXNlIjoiaWQiLCJhdXRoX3RpbWUiOjE2MzI0NTk1NDEsIm5hbWUiOiJDb2R5IE1jRG9uYWxkIiwiZXhwIjoxNjMyNDYzMTQxLCJpYXQiOjE2MzI0NTk1NDEsImp0aSI6IjVkOWI2ZTU5LWI1NDgtNGM4Yy05MjcxLTUxZTY1NzNkOTAzYiIsImVtYWlsIjoiY29keS5tY2RvbmFsZEByZXZhdHVyZS5uZXQifQ.3Jpjc-gkNez14h7F4GvkI3vcbV0Nx39yt9LrqYTREBpsw4G01xY1N-S33q75TGdTgfCvUne5yzH2NEcj55tt-oLjBqqtDhNFcVSKstHqI0LCwcTHLs9qArwhq2nxgPff7n3sHQOMMU6fHEr3bpMnfWvRozRxqkeFqLwwx4biK0_OBj_Y5P0kRIZCaq_g2OF850NkuMre-QYDIkFLkh3X15_DqyTJ_Y5Zhb7oJZfYtfZHTpW3KqU6-88pCFTwaLt5TYZAimbUGZhHl1yQpjPDM-EkTq8A_d8U6Pn0IlyXvJ_7LvtqC9XSF9idiaWhDGlDrwcELTZ6-Do7asp0LeOwNw",
        "CognitoIdentityServiceProvider.client_id.LastAuthUser": "example_user",
        "CognitoIdentityServiceProvider.client_id.example_user.clockDrift": "-1",
        "CognitoIdentityServiceProvider.client_id.example_user.userData": "{\"UserAttributes\":[{\"Name\":\"sub\",\"Value\":\"example_user_id\"},{\"Name\":\"email_verified\",\"Value\":\"true\"},{\"Name\":\"name\",\"Value\":\"Test User\"},{\"Name\":\"email\",\"Value\":\"example.email@test.net\"}],\"Username\":\"example_user\"}"
    },
    "keyPrefix": "CognitoIdentityServiceProvider.client_id",
    "userDataKey": "CognitoIdentityServiceProvider.client_id.example_user.userData",
    "attributes": {
        "sub": "example_user_id",
        "email_verified": true,
        "name": "Test User",
        "email": "example.email@test.net"
    },
    "preferredMFA": "NOMFA"
}
```
