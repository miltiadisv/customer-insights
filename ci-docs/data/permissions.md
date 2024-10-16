---
title: "Assign user permissions"
description: "Learn about permissions and user roles."
ms.date: 09/01/2023
ms.reviewer: mhart
ms.topic: conceptual
author: pkieffer
ms.author: philk
---

# Assign user permissions

[!INCLUDE [consolidated-sku](./includes/consolidated-sku.md)]

Access to Dynamics 365 Customer Insights - Data is restricted to users in your organization that are added to the application by an admin. An admin can add, edit, or remove users. A user can be a single user, group, or application. There are different types of roles a user can have:

## Viewer

- Explore insights and segments within the **Home** and **Segments** pages.
- Search and filter customer profiles using the **Customers** page. Fields must be searchable.
- View and explore the **Enrichment** page.
- Explore and export tables using the **Tables** page.
- View the status of system processes using the **System** page.
- View exports in the **Exports** page.

## Marketing contributor (preview)

[!INCLUDE [public-preview-banner](includes/public-preview-banner.md)]

- The Marketing contributor role is only available in [business unit enabled environments](business-units-data-separation.md)
- Can only access customer profiles that belong to the business unit of the user.
- Create segments using the **Segments** page (only *Build your own*, no projected attributes).
- Create measures using the **Measures** page (only *Build your own*). Can only create measures on tables that have a relationship path to customer profiles.

> [!NOTE]
> Marketing contributors can only create segments and measures from customer profiles, unified activities, segments, and customer measures. This permission has limited functionality in some areas compared to the Contributor role.
> Marketing contributors can't search for customers in the *customers* view.

[!INCLUDE [public-preview-note](includes/public-preview-note.md)]

## Contributor

- All permissions available to the Viewer.
- Load and transform data using the **Data sources** page.
- Complete **Data Unification** which result in the unified customer profile table.
- Define **Relationships** and **Activities**.
- Create segments using the **Segments** page.
- Create measures using the **Measures** page.
- Manage configuration and enrich customer profiles from the **Enrichment** page (for first party enrichments only).
- Manage and create exports based on [connections shared with contributors](connections.md#allow-contributors-to-use-a-connection-for-exports).

## Admin

- All permissions available to the Contributor.
- Change settings on the **System** page, including the working language, refresh schedules for your system processes, and exporting diagnostic logs.
- Change settings on the **Permissions** page, including users, API keys, private links, and key vault.
- Set search and filter definitions for the Customers page using the **Search & filter index** page (accessible via the **Customers** page).
- Manage connections and allow them for other user roles on **Connections** page.
- Manage configuration and enrich customer profiles from the **Enrichment** page (for all enrichments).
- Manage and create exports on the **Exports** page.
- Install and use the **Customer Card Add-in**.
- Add and use the **Power Apps connector**.
- Enable usage of [APIs](apis.md).
- [Assign environment ownership](manage-environments.md#change-the-owner-of-an-environment) to another admin.

## Admin (owner)

- All permissions available to the Admin.
- [Reset and delete](manage-environments.md#reset-an-existing-environment-preview) the environment.

## Add users

1. Go to **Settings** > **Permissions** and select the **Users** tab.

1. Select **Add users** to open the **Add/Edit permissions** pane.

1. Use the **Search** field to find the user or group you want to add. Select a **Role** to assign to that user or group.

1. Select **Save**. The current environment is automatically shared with the user or members of the group. Users can access the app and work according to their specified role.

## View current permissions

Go to **Settings** > **Permissions** and select the **Users** tab to view the list of active users and their role assignments. You can sort the list of users by any column or use the search box to find a particular user.

## Manage current users

Go to **Settings** > **Permissions** and select the **Users** tab. You can sort the list of users by any column or use the search box to find the user you want to manage.

Select a user to view available actions.

- **Edit** to edit the user's role in Customer Insights - Data. Select **Save** to confirm the change.
- **Remove** to revoke the user's access. Select **Delete** to confirm the deletion.

It can take up to 15 minutes to fully propagate the changes to permissions. To see changes reflected in the user interface, users should refresh the browser window that runs the application.

[!INCLUDE [footer-include](includes/footer-banner.md)]
