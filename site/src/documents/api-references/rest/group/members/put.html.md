---

title: 'Create Group Member'
category: 'Group'

keywords: 'put'

---


Add a member to a group.

Method
------

PUT `/group/{id}/members/{userId}`

Parameters
----------

#### Path Parameters

<table class="table table-striped">
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>id</td>
    <td>The id of the group</td>
  </tr>
  <tr>
    <td>userId</td>
    <td>The id of user to add to the group</td>
  </tr>
</table>



Result
------

This method returns no content.


Response codes
--------------

<table class="table table-striped">
  <tr>
    <th>Code</th>
    <th>Media type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>204</td>
    <td></td>
    <td>Request successful.</td>
  </tr>
  <tr>
    <td>403</td>
    <td>application/json</td>
    <td>Identity service is read-only (Cannot modify users / groups / memberships).</td>
  </tr>
  <tr>
    <td>500</td>
    <td>application/json</td>
    <td>In case an internal error occurs. See the <a href="ref:#overview-introduction">Introduction</a> for the error response format.</td>
  </tr>
</table>

Example
-------

#### Request

PUT `/group/sales/members/jonny1`


#### Response

Status 204. No content.