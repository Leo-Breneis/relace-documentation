# Relace Documentation
This is the documentation for the Rest API from Relace

## What is Relace?

Relace is a Website that you can use to have all of your Homeworks at one place

You can find your current Front-End at [relacexyz](https://relacexyz.duckdns.org)

### Who are we?

We are three students from the HTBLA Leonding and this a school project from us.

We are:

| Eros            | Leo            | Daniel    |
|-----------------|----------------|-----------|
| mainly frontend | mainly backend | teams api |

<note> If you want to use this API you will have to ask us for AccessAllowOrigin</note>


## How to use the REST API

<tip>Parameters that are <b>bold</b> are required Parameters</tip>
<tip>Parameters that are <i>cursive</i> are optional Parameters</tip>


| API call                | endpoint             | Parameters                                                                                                                                                                                                                                                                                         | return values                                                                                           |
|-------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| login                   | /auth/login          | **username** `: String` <br/> **password** `: String`                                                                                                                                                                                                                                              | success `: bool`<br/> message `: String`<br/> jwt `: String`<br/> refreshToken `: String`               |
| register                | /auth/register       | **username** `: String` <br/> **password** `: String`<br/> **email** `: String`                                                                                                                                                                                                                    | success `: bool`<br/> message `: String`                                                                |
| get assignments         | /a/get               | **jwt** `: String`<br/> *count* `: int` `all`<br/>  *offset* `: int` `0`<br/> *compact* `: boolean` `false`<br/> *searchParams* `: String` DEF:`emtpy` <br/> *course* `: String` `empty`<br/>  *after* `: long` `0`<br/> *before* `: long` `unlimited`<br/>*order* `: String` (asc or desc) `desc` | success `: bool`<br/> message `: String`<br/> [assignments](Assignment-Formatation.md) `: Assignment[]` |
| set token               | /auth/tpapi/settoken | **jwt** `: String`<br/> **token** `: String`<br/>  **key** `: String` <br/>**api** `: String`                                                                                                                                                                                                      | success `: bool`<br/> message `: String`                                                                |
| has token ?             | /auth/tpapi/hastoken | **jwt** `: String`<br/> **api** `: String`                                                                                                                                                                                                                                                         | success `: bool`<br/> message `: String`                                                                |
| load moodle assignments | /a/loadmoodle        | **jwt** `: String`<br/> **key** `: String`                                                                                                                                                                                                                                                         |                                                                                                         |


<warning>You have to put https://relacexyz.duckdns.org/api in front of every endpoint!</warning>
