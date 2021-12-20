<!-- loioe4b4b5f9a64d46d08ceec5488a108008 -->

# When to Use Which Account Model

Determine which account model with subaccounts is the most appropriate for your needs.

The tables below provide requirements with regards to project and team setup as well as the services and resources involved. You can compare them against your own requirements and see which account model most closely matches. Please remember that the four account models are a result of a best-practice approach. They are not mutually exclusive and you may want to use a combination of approaches, if, for example, you have different projects with different requirements.



<a name="loioe4b4b5f9a64d46d08ceec5488a108008__section_bmz_2xh_cgb"/>

## Project Setup


<table>
<tr>
<th valign="top">

Your Requirements ...



</th>
<th valign="top">

Account Model 1



</th>
<th valign="top">

Account Model 2



</th>
<th valign="top">

Account Model 3



</th>
<th valign="top">

Account Model 4



</th>
<th valign="top">

Account Model 5



</th>
</tr>
<tr>
<td valign="top">

You follow the DevOps methodology and have many autonomous projects.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

\(X\)



</td>
</tr>
<tr>
<td valign="top">

You need different stages for your project or scenario.



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

X



</td>
</tr>
<tr>
<td valign="top">

You have a highly centralized project landscape with many projects using the same technologies \(for example, Fiori development for a Fiori launchpad\).



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
</tr>
<tr>
<td valign="top">

You want to share more expensive resources \(HANA databases, Integration service tenants\) with multiple projects.



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

\(X\)



</td>
</tr>
</table>



<a name="loioe4b4b5f9a64d46d08ceec5488a108008__section_b44_kxh_cgb"/>

## Team Setup


<table>
<tr>
<th valign="top">

Your Requirements ...



</th>
<th valign="top">

Account Model 1



</th>
<th valign="top">

Account Model 2



</th>
<th valign="top">

Account Model 3



</th>
<th valign="top">

Account Model 4



</th>
<th valign="top">

Account Model 5



</th>
</tr>
<tr>
<td valign="top">

You have a large number of developers, with several different project admins responsible for them.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
</tr>
<tr>
<td valign="top">

You have many different development teams, but only one single production environment for which the teams develop applications.



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

You have different development teams, each of which works independently, meaning they should not be able to, for example, accidentally break the other team's developments.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
</tr>
<tr>
<td valign="top">

Your development teams on SAP BTP are coming from different organizational units in different geographic locations and you want to track them separately.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
</tr>
<tr>
<td valign="top">

You want to ensure that no developer or project admin can assign privileges to themselves for services or applications.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

You have stringent security requirements. For example, you don't want all developers to have access to all Git repositories.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

\(X\)



</td>
</tr>
<tr>
<td valign="top">

You want to allow access to on-premise systems via Cloud Connector only for selected projects, while restricting it for the applications of other projects.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

 



</td>
<td valign="top">

\(X\)



</td>
</tr>
</table>



<a name="loioe4b4b5f9a64d46d08ceec5488a108008__section_rwz_lxh_cgb"/>

## Services and Resources


<table>
<tr>
<th valign="top">

Your Requirements ...



</th>
<th valign="top">

Account Model 1



</th>
<th valign="top">

Account Model 2



</th>
<th valign="top">

Account Model 3



</th>
<th valign="top">

Account Model 4



</th>
<th valign="top">

Account Model 5



</th>
</tr>
<tr>
<td valign="top">

You want to assign quotas to different projects and tightly control that the projects don't exceed their resources.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
<td valign="top">

\(X\)



</td>
</tr>
<tr>
<td valign="top">

You want to allow the usage of a particular service only for selected projects.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

 



</td>
<td valign="top">

\(X\)



</td>
</tr>
<tr>
<td valign="top">

You want to easily monitor which services are consumed by which projects. For example, you might want to do internal billing based on the resource consumption of the individual projects.



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

X



</td>
<td valign="top">

\(X\)



</td>
<td valign="top">

X



</td>
</tr>
<tr>
<td valign="top">

You want to restrict the exposure of on-premise systems through central middleware \(Integration service\) or an API layer \(API Management\).



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

X



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
</table>

-   X: Account model meets this requirement.

-   \(X\): Account model meets this requirement with restrictions.


