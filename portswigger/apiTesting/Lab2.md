# Lab: Finding and exploiting an unused API endpoint

[Lab](https://portswigger.net/web-security/api-testing/lab-exploiting-unused-api-endpoint)

## Information Gathering

### Discovering API documentation

![Untitled](images/Lab2/1.png)

![Second Picture](images/Lab2/2.png)

there doesn’t seem to be a API documentation in place.

### Discovering API Endpoints

![Second Picture](images/Lab2/3.png)

![Second Picture](images/Lab2/4.png)

![Second Picture](images/Lab2/5.png)


### Examining API Endpoints

#### Change Parameters

![Second Picture](images/Lab2/6.png)


#### Change HTTP methods

PATCH

![Second Picture](images/Lab2/7.png)

This indicates, that the PATCH HTTP method is allowed.

Furthermore the HTTP method requires a application/json Content-Type

→ this looks like a potential attack surface

#### Examine the JSON Format

![Second Picture](images/Lab2/8.png)

![Second Picture](images/Lab2/9.png)

## Exploit

![Second Picture](images/Lab2/10.png)

![Second Picture](images/Lab2/11.png)

Boom 🪄

![Second Picture](images/Lab2/12.png)

Move on adding the product to your cart and then purchase the item for free.

![Second Picture](images/Lab2/13.png)
