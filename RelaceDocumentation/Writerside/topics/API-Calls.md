# Relace Documentation
This is the documentation for the Rest API from Relace

## What is Relace?

Relace is a website where you can see all of your homeworks at one place

You can find your current frontend at [relacexyz](https://relacexyz.duckdns.org)

### Who are we?

We are three students from the HTBLA Leonding and this a school project from us.

We are:

| name                   | Eros            | Leo             | Daniel    |
|------------------------|-----------------|-----------------|-----------|
| area of responsibility | mainly frontend | mainly backend  | teams api |
| discord                | 178laflame178   | opfisoftlover69 | -         |

<note> If you want to use this API you will have to ask us for AccessAllowOrigin</note>


## How to use the REST API

<tip>Parameters that are <b>bold</b> are required Parameters</tip>
<tip>Parameters that are <i>cursive</i> are optional Parameters</tip>


| API call                | endpoint             | Parameters                                                                                                                                                                                                                                                                                         | return values                                                                                                   |
|-------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| login                   | /auth/login          | **username** `: String` <br/> **password** `: String`                                                                                                                                                                                                                                              | success `: bool`<br/> message `: String`<br/> jwt `: String`<br/> refreshToken `: String`                       |
| register                | /auth/register       | **username** `: String` <br/> **password** `: String`<br/> **email** `: String`                                                                                                                                                                                                                    | success `: bool`<br/> message `: String`                                                                        |
| get assignments         | /a/get               | **jwt** `: String`<br/> *count* `: int` `all`<br/>  *offset* `: int` `0`<br/> *compact* `: boolean` `false`<br/> *searchParams* `: String` DEF:`emtpy` <br/> *course* `: String` `empty`<br/>  *after* `: long` `0`<br/> *before* `: long` `unlimited`<br/>*order* `: String` (asc or desc) `desc` | success `: bool`<br/> message `: String`<br/> [assignments](Assignment-Formatation.md) `: Assignment[]`         |
| set token               | /auth/tpapi/settoken | **jwt** `: String`<br/> **token** `: String`<br/>  **key** `: String` <br/>**api** `: String`                                                                                                                                                                                                      | success `: bool`<br/> message `: String`                                                                        |
| has token ?             | /auth/tpapi/hastoken | **jwt** `: String`<br/> **api** `: String`                                                                                                                                                                                                                                                         | success `: bool`<br/> message `: String`                                                                        |
| load moodle assignments | /a/loadmoodle        | **jwt** `: String`<br/> **key** `: String`                                                                                                                                                                                                                                                         | success `: bool`<br/> message `: String`                                                                        |
| get all courses         | /c/get               | **jwt** `: String`                                                                                                                                                                                                                                                                                 | success `: bool`<br/> message `: String`<br/> [courses](Assignment-Formatation.md) `: Courses`                  |
| get by id               | /a/getbyid/          | **jwt** `: String`<br/> **id** `: int`                                                                                                                                                                                                                                                             | success `: bool`<br/> message `: String`<br/> [assignment](Assignment-Formatation.md) `: Assignment` (Extended) |

<warning>You have to put https://relacexyz.duckdns.org/api in front of every endpoint!</warning>
