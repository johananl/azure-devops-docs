---
title: Manage paid access for users in Azure DevOps
titleSuffix: Azure DevOps
ms.custom: seodec18
description: Assign paid access and control the default access of your new users in Azure DevOps.
ms.technology: devops-billing
ms.assetid: 02cb8774-6d1d-4f15-8818-b56541033b1f
ms.topic: conceptual
ms.author: chcomley
author: chcomley
ms.date: 03/31/2021
monikerRange: '<= azure-devops'
---

# Manage paid access for users

[!INCLUDE [version-all](../../includes/version-all.md)]

> [!NOTE]
> We've recently simplified Azure DevOps billing, so now rather than complete a purchase process, you assign and remove users. You're billed according to these assignments. This article is repurposed to help you take advantage of the tools we have for managing paid access for users. This way you only pay for what you need.

Learn how to manage paid access to [Azure Boards](https://azure.microsoft.com/services/devops/boards/), [Azure Repos](https://azure.microsoft.com/services/devops/repos/) and [Azure Test Plans](https://azure.microsoft.com/services/devops/test-plans/).

Visual Studio subscribers get access included with their subscription, and their subscription is detected when they sign in to Azure DevOps for the first time.

[!INCLUDE [pricing-calculator-tip](../../includes/pricing-calculator-tip.md)]

::: moniker range=" < azure-devops"

## Prerequisites

Ensure the following is true:

* [Licensing is set up for your organization via Azure](https://azure.microsoft.com/pricing/details/devops/server/)
* You have [Project Collection Administrator or organization Owner permissions](../security/lookup-organization-owner-admin.md)

## Pay through Azure

Complete the following steps to pay via Azure.

1. Set up an Azure DevOps organization, even if you don't intend to use it.
2. During this process, set up billing using an Azure subscription and buy users or CI/CD.
3. Assign licenses to users.
You're entitled to the same amount of user licenses to be used in the server.

::: moniker-end

::: moniker range="azure-devops"
## Prerequisites

Ensure the following is true:

* [Billing is set up for your organization](set-up-billing-for-your-organization-vs.md)
* You have [Project Collection Administrator or organization Owner permissions](../security/lookup-organization-owner-admin.md)

<a name="buy-access-vs-marketplace"></a>

## Assign users Basic or Basic + Test Plans

The simplest way to control paid access is by manually assigning an access level when you [add a new user to your organization](../accounts/add-organization-users.md) and by [removing users](../accounts/delete-organization-users.md) when they leave your organization. 

Keep the following information in mind:

- **Visual Studio subscribers** are detected automatically when they sign in. There's no additional charge for users with a Visual Studio subscription.
- **Stakeholder** is a [free access level with limited functionality](../security/get-started-stakeholder.md).
- **Basic** is free for the first 5 users, and paid for 6 or more users.
- **Basic + Test Plans** is paid only, but is [free to try for 30 days](try-additional-features-vs.md).

## Select the default access level for new users

After you set up billing for your organization all new users get the free Stakeholder access if they're added directly to a Project. That way you aren't surprised by charges for new users who weren't added directly to the organization by a Project Collection Administrator. 

To change the access level for new users added to projects, do the following tasks:

1. Sign in to your organization (```https://dev.azure.com/{yourorganization}```).

2. Select ![gear icon](../../media/icons/gear-icon.png) **Organization settings**.

   ![Open Organization settings](../../media/settings/open-admin-settings-vert.png)

3. Select **Billing**.

   :::image type="content" source="media/shared/select-billing-organization-settings.png" alt-text="Select Billing settings":::

4. Change **Default access level for new users** to Basic.

   :::image type="content" source="media/shared/default-access-level-basic.png" alt-text="Default access level for new users to Basic":::

## Automate access level assignment with group rules

Larger organizations may want to automate access level assignments, so you don't have to manually do so every time a user is added or removed. [Group rules](../accounts/assign-access-levels-by-group-membership.md) are a great way to automate access level assignment for your organization, and under assignment-based billing, you'll find that assignment errors are no longer very common.

## Reduce charges for users who no longer need access

Billing stops automatically when users are removed from your organization or are assigned the free Stakeholder access level. 
 
To find out if you have users who are no longer using Azure DevOps, do the following tasks:

1. Sign in to your organization (```https://dev.azure.com/{yourorganization}```).

2. Select ![gear icon](../../media/icons/gear-icon.png) **Organization settings**.

   ![Open Organization settings](../../media/settings/open-admin-settings-vert.png)

3. Select **Users** and then sort by **Last Access**.

   :::image type="content" source="media/shared/last-access.png" alt-text="Select Users and then sort by Last Access":::
 
4. If you have users who've never signed in, you can find out how recently they were added by exporting the list of users and checking the **Date Created** column. 

   :::image type="content" source="media/shared/export-users.png" alt-text="Export users":::

## Pay for a user once across multiple organizations

If you have more than one Azure DevOps organization, you can turn on multi-organization billing and pay for each **Basic** or **Basic + Test Plans** user once, for all organizations under the same billing Azure subscription. For more details, see [multi-organization billing FAQs](./billing-faq.yml). Complete the following steps.

1. Sign in to your organization (```https://dev.azure.com/{yourorganization}```).

2. Select ![gear icon](../../media/icons/gear-icon.png) **Organization settings**.

   ![Open Organization settings](../../media/settings/open-admin-settings-vert.png)

3. Select **Billing**.

   ![Select Billing from Organization settings](media/shared/select-billing-organization-settings.png)

4. Select **Configure user billing**.
   
   ![Select Configure user billing](media/buy-more-basic-access/select-configure-user-billing.png)

5. Select **Multi-organization**, and then select **Save**.

   ![Select Multi-organization](media/buy-more-basic-access/select-multi-organization-billing.png)

::: moniker-end
## Next steps

> [!div class="nextstepaction"]
> [Buy parallel jobs](../../pipelines/licensing/concurrent-jobs.md#how-much-do-parallel-jobs-cost)