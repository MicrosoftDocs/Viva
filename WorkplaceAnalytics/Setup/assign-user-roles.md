---

title: Workplace Analytics Setup -- Assign roles to admins, analysts, and PMs 
description: How to assign roles in Workplace Analytics for admins, analysts, and program managers
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
audience: Admin
---

# Assign user roles 

**Role:** AAD admin 

In the following procedures, you identify a user by using their user identifier.  

## Assign one role to a user 

1. Log in to your tenant's Azure Active Directory admin center. 

2. In the left navigation menu, select **Enterprise Applications**:

   ![Enterprise applications](../images/wpa/setup/enterprise-apps.png) 
   
   This opens the **Enterprise Applications | All applications** page of the dashboard. 

3. In the **Application Type** drop-down menu, select **All Applications**. 

4. In the search field, type "workplace" and then press **Enter**. 

5. In the search results, select **Workplace Analytics**. This opens the **Workplace Analytics | Overview** page.  

6. On the **Overview** page, under **Getting Started**, select **Assign users and groups**: 

   ![Overview page](../images/wpa/setup/wpa-overview.png)  

7. On the Workplace Analytics **Users and groups** page, select **Add user**:

   ![Overview page](../images/wpa/setup/wpa-users-and-groups.png)  

This opens the **Add Assignment** page. 

> [!Note] 
> In the **Users and groups** area, “None Selected” currently appears. 

8. On the **Add Assignment** page, select **Users and groups**: 
   
   ![Overview page](../images/wpa/setup/select-users-and-groups-4.png)

   This opens the **Users and groups** pane on the right side of the page.

9. Under **Users and groups**, identify the user to whom you want to assign a role. Start typing that person’s user identifier in the search field and then select their identifier in the results list. After you have selected the person, their identifier appears in the right pane under **Selected items**: 


> [!Note] 
> In the Users and groups area, the count of selected users has changed to 1: 


10. On the Add Assignment page, select Select Role. This opens the Select Role pane on the right side of the page: 

 
11. From the list that appears, select one of the following roles:  

* Analyst 
* Analyst (Limited Access) 
* Administrator 
* Program manager 
* Group manager 

The role you selected appears at the bottom of the Select Role pane: 


The role also appears under Add Assignment in the Select Role area: 


> [!Note] 
> To change the role to assign to this user, repeat steps 10 and 11 and select a different role in step 11. 

12. After you’ve chosen the user and the role for that user, select Assign at the bottom of the Add Assignment page: 
 

After a few seconds, a message in the upper right informs you of the success of the role assignment:  


You have now assigned one role to one user.  

13. (Optional) You can now assign additional roles, either to the same user or to different users. To select other users and assign roles to them, repeat steps 7-12 in this procedure. To add another role to the same user, see Assign an additional role to a user.  

## Verify role assignments 

Use this procedure to see what roles have been assigned to a user.  

1. On the Workplace Analytics Users and groups page, start typing the user identifier. As you do so, the list of users and groups filters to contain the name you’re typing.  

2. Find the user in the list. Their role appears in the Role assigned column.  

## Assign an additional role to a user 

1. On the Workplace Analytics Users and groups page, select Add user. This opens the Add Assignment page. 

> [!Note] 
> In the Users and groups area, “None Selected” currently appears. 

2. On the Add Assignment page, select Users and groups: 


This opens the Users and groups pane on the right side of the page: 

 
3. Under Users and groups, identify the user to whom you want to assign a role. In this case, it’s a user who already has a role. Start typing that person’s user identifier in the search field and then select their identifier in the results list. After you have selected the person, their identifier appears in the right pane under Selected items: 
 

> [!Note] 
> In the Users and groups area, the count of selected users has changed to 1: 

 
4. On the Add Assignment page, select Select Role. This opens the Select Role pane on the right side of the page: 

 
5. From the list that appears, select one of the following roles:  

* Analyst 
* Analyst (Limited Access) 
* Administrator 
* Program manager 
* Group manager 

The role you selected appears at the bottom of the Select Role pane: 


The role also appears under Add Assignment in the Select Role area: 


> [!Note] 
> If you want to change role that you’re about to assign to this user, you can do so by repeating steps 4 and 5 and selecting a different role in step 5. 

6. After you’ve chosen the user and the correct role for that user, select Assign at the bottom of the Add Assignment page: 
 

After a few seconds, a message in the upper right informs you of the success of the role assignment:  

 
You have now assigned another role to this user. If you verify the role assignments of this user, you can see in the table all roles that the user has assigned:  
