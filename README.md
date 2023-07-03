# spring-boot-2.5.4-java8-securityJWT-jpa
spring-boot-2.5.4-java8-securityJWT-jpa

Características:
- Spring boot 2.5.4
- Java 1.8
- Spring security
- Authentication
- Authorization

credenciales
```java
@Override
  public void run(String... params) throws Exception {
    AppUser admin = new AppUser();
    admin.setUsername("admin");
    admin.setPassword("admin");
    admin.setEmail("admin@email.com");
    admin.setAppUserRoles(new ArrayList<AppUserRole>(Arrays.asList(AppUserRole.ROLE_ADMIN)));

    userService.signup(admin);

    AppUser client = new AppUser();
    client.setUsername("client");
    client.setPassword("client");
    client.setEmail("client@email.com");
    client.setAppUserRoles(new ArrayList<AppUserRole>(Arrays.asList(AppUserRole.ROLE_CLIENT)));

    userService.signup(client);
  }
