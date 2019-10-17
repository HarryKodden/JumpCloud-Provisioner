# JumpCloud Provisioner

This Python module can be used to provision USERS and GROUPS to a JumpCloud subscription

## Prerequisites

In order to use this module, you need to have a JumpCLoud registration first.
You can register at https://jumpcloud.com/ and sign up.

As a registered user you can obtain an API key.

## Using the Module

In your Python Application import this module:

˜˜˜
from jumpcloud import JumpCloud
˜˜˜

Initializing the JumpCloud Class:

˜˜˜
    jumpcloud = JumpCloud(
       "https://console.jumpcloud.com",
       YOUR-API-KEY
    )
 ˜˜˜

 Register a USER with the **person()** method:

˜˜˜
    jumpcloud.person(
            username = "harry",
            firstname = "Harry",
            lastname = "Koddem",
            email = "harry@e-tunity.nl",
            sshPublicKeys = [])
        )
˜˜˜

Register a GROUP with the **group()** method:

˜˜˜
	jumpcloud.group("My First Group", [ "harry" ])
˜˜˜

Calling the **cleanup()** method, will remove existing USERS, GROUPS and GROUP-MEMBERS from your JumpCloud organization that ar not re-declared.

˜˜˜
	jumpcloud.cleanup()
˜˜˜



