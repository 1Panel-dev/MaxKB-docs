# Login Authentication
!!! Abstract ""
    MaxKB Professional Edition supports LDAP, CAS, OIDC, OAUTH2 single sign-on protocols, as well as WeChat Work, DingTalk, and Lark mobile QR code login verification, meeting enterprise requirements for strong identity verification and access control.

## 1 LDAP

!!! Abstract ""
    The LDAP configuration process can be referenced in the image below. Note that this feature is enabled by checking "Enable LDAP Authentication" at the bottom.
    Tip: After configuration, you can click "Test Connection" at the top to instantly test if the configuration information is correct and the network is connected.
![LDAP](../../img/system/LDAP.png)


## 2 CAS

!!! Abstract ""
    The CAS configuration process can be referenced in the image below.
    **Note:** The CAS callback URL is the MaxKB access URL plus `/api/cas`, for example: `http://40.100.86.240:8080/api/cas`
![CAS](../../img/system/CAS.png)


## 3 OIDC

!!! Abstract ""
    The OIDC configuration process can be referenced in the image below.
    **Note:** The OIDC callback URL is the MaxKB access URL plus `/api/oidc`, for example: `http://40.100.86.240:8080/api/oidc`
![OIDC](../../img/system/OIDC.png)

## 4 OAuth2

!!! Abstract ""
    The OAUTH2 configuration process can be referenced in the image below (using GitHub as an example authorization provider).
    **Note:** The OAUTH2 callback URL is the MaxKB access URL plus `/api/oauth2`, for example: `http://40.100.86.240:8080/api/oauth2`
![OAHTU2](../../img/system/oauth2.png)

## 6 Login Authentication

!!! Abstract ""
    After completing authentication configuration, select the corresponding authentication method on the login page to log in.
![Login Authentication](../../img/system/auth_login.png)
