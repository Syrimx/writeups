#Lab: Finding and exploiting an unused API endpoint


# Information Gathering

## Discovering API documentation

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/6cb3f64c-ed31-4d9c-80d1-ac8d0ca019d2/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/ee29dfba-6e88-4bd4-8b85-899a4d8211b6/Untitled.png)

there doesn’t seem to be a API documentation in place.

## Discovering API Endpoints

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/4c60b452-257d-4c3d-b469-b6a59eeb97d6/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/0bfc5715-3ac7-4c29-9525-4fc0d45d0740/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/5d31ccc8-2b12-4388-a349-0e705ad594b8/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/4ef7e63b-08f6-4b69-9a16-ff9dd8a26bb1/Untitled.png)

## Examining API Endpoints

### Change Parameters

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/f38e2f4b-4501-43f2-9cfe-11d4a5d78e25/Untitled.png)

### Change HTTP methods

PATCH

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/158ca07a-f786-4b5e-8efe-447c80ee6924/Untitled.png)

This indicates, that the PATCH HTTP method is allowed.

Furthermore the HTTP method requires a application/json Content-Type

→ this looks like a potential attack surface

### Examine the JSON Format

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/08099cbd-ad54-4812-962a-e6313633447c/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/aa5272c0-9f7a-428b-a371-f536ea5a70f2/Untitled.png)

# Exploit

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/9fc5ba01-3fa1-4d7f-87af-c52302ef1137/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/f7ca8509-4b70-4dec-b952-3be9a2b1e128/Untitled.png)

Boom 🪄

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/0d9d9f1d-2ee7-4105-90b5-81dc34e79050/Untitled.png)

Move on adding the product to your cart and then purchase the item for free.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/006f0191-f01c-4731-a492-e6276193f468/cc5e31e9-7ea4-4046-ae8a-ff9347204fdc/Untitled.png)