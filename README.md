<p align="left">
  <img width="600" height="400" src="https://github.com/GluuFederation/agama-ldap/assets/43112579/639a8ca4-7549-4167-a5eb-5fe19fad3ff5">
</p>

[![Contributors][contributors-shield]](contributors-url)
[![Forks][forks-shield]](forks-url)
[![Stargazers][stars-shield]](stars-url)
[![Issues][issues-shield]](issues-url)
[![Apache License][license-shield]](license-url)

# Gluu agama-ldap

Welcome to the [https://github.com/GluuFederation/agama-ldap](agama-ldap) project.
This project is governed by [Gluu](https://gluu.org) and published under an
Apache 2.0 license. It provides various flows to password authenticate a person.

Password authentication is still useful ! ! !

This is also a great project to fork if you want to write
a “Hello World” Agama project.

## Implementations

* Jans Auth Server
* Gluu Flex

## Flow: One-step password authn

This is the classic combined username / password form authentication workflow.
The sequence diagram below shows the good flow.

![agama-ldap sequence diagram image](Agama-LDAP-PW-sequence.png)
[Source](https://sequencediagram.org/index.html#initialData=C4S2BsFMAIEEHMCGBbRBaACgdWgCUQA4ECe0AYuAPYDuAULYgMbCUBO0BkrAzpQHa0CiVqEYghfYNABGrGty61IksKWqRp3MJEHDR4xJOgBJACIZa0ygFc+AE2GlE14AAtloxMB2CuvPmgAfGYYAFzQxJDcHFCICgB0iSbQ1IZSLNBU8CACIUGy8lzh1iB2APQE1ORsyL48-Ply1Aqs4YyskHbclk0tQSHhGADyAMoAKtWstXmBzm4eIIxekOEAbojgpcsAFCV2ADQc1ACUDC7uKkve-ebhAN4ARB3c1uDAD6EPL4yMUdwP+wAOnwHoxKHZIB9oAAmAAMsKBIOQf0Q8Eh4QeQwA0g8AL60GYFZpFaBDTh8MzQMEQnqFVhBdSabRtDbgaRMADWQA)

# Flow Configuration
Below is a typical agama-ldap flow
  ```
        {
            "org.gluu.agama.ldap.pw.main": {
                "flowConfig" : {
                    "MAX_LOGIN_ATTEMPT": "6",
                    "ENABLE_LOCK": "true",
                    "LOCK_EXP_TIME": "180"
                }
            }
        }
  ```
- MAX_LOGIN_ATTEMPT: Is the maximum failed login attempt before the user account is locked
- ENABLE_LOCK: true/false, this is use to enable the Account Lock feature
- LOCK_EXP_TIME: The time in seconds befor a locked account is unlock.
  

# License

This project is licensed under the [Apache 2.0](https://github.com/GluuFederation/agama-ldap/blob/main/LICENSE)


<!-- This are stats url reference for this repository -->
[contributors-shield]: https://img.shields.io/github/contributors/GluuFederation/agama-ldap.svg?style=for-the-badge
[contributors-url]: https://github.com/GluuFederation/agama-ldap/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/GluuFederation/agama-ldap.svg?style=for-the-badge
[forks-url]: https://github.com/GluuFederation/agama-ldap/network/members
[stars-shield]: https://img.shields.io/github/stars/GluuFederation/agama-ldap?style=for-the-badge
[stars-url]: https://github.com/GluuFederation/agama-ldap/stargazers
[issues-shield]: https://img.shields.io/github/issues/GluuFederation/agama-ldap.svg?style=for-the-badge
[issues-url]: https://github.com/GluuFederation/agama-ldap/issues
[license-shield]: https://img.shields.io/github/license/GluuFederation/agama-ldap.svg?style=for-the-badge
[license-url]: https://github.com/GluuFederation/agama-ldap/blob/main/LICENSE
