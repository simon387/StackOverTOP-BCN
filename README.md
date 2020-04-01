# StackOverTOP-BCN

## 1

Fabio: 
Credo possa servire a tutti...a me è successo inspiegabilmente dopo il cambio di orario e c'ho sbattuto la testa alla grande ma ce l'ho fatta. Se per qualche motivo un giorno dovesse venirvi fuori questo: **The server time zone value 'CEST' is unrecognized or represents more than one time zone. You must configure either the server or JDBC driver (via the serverTimezone configuration property) to use a more specifc time zone value if you want to utilize time zone support.**

La soluzione è questa: 
```java
String timeZone = TimeZone.getDefault().getID();
// Hibernate settings equivalent to hibernate.cfg.xml's properties
Properties settings = new Properties();
settings.put(org.hibernate.cfg.Environment.DRIVER, "com.mysql.cj.jdbc.Driver");
settings.put(org.hibernate.cfg.Environment.URL, "jdbc:mysql://"+dbUrl+":"+dbPort+"/"+dbName+"+?serverTimezone="+timeZone+"");
```

---

## 2

Cristian:
NON RIMUOVERE MAI i loghetti **"powered by Google"** dai vari servizi ( autocomplete, mappe etc ) perchè Google, prima o poi se ne accorgerà e vi bloccherà il servizio su quel dominio.

---



