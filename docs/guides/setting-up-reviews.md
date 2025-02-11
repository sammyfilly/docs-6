---
sidebar_label: Setting up Reviews
title: Setting up Reviews for Team Workflows  
---

You can enable reviews for all Statsig resources such as feature gates, dynamic configs, segments, and experiments that you'll likely deploy to a production environment. 

### Turning on Change Reviews for a Project
As a Project Admin, you can configure your project to require reviews for any changes. To enable reviews for your project, 
 - Navigate to the **Project Settings** page 
 - Click on the **Edit** button next to **Config Review Requirements**

![Screen Shot 2021-12-15 at 4 21 02 PM](https://user-images.githubusercontent.com/1315028/146821144-2c95de68-683f-4490-877d-3c95204ad83c.png)

- Select **Reviews Required** from the drop down list

<img width="455" alt="image" src="https://user-images.githubusercontent.com/1315028/166673961-3da1f147-47fc-458b-aae1-4ed73ba3a73e.png"/>

- You can optionally allow yourself as a project admin to bypass the review requirement and self-approve review requests.

- Now when you make any configuration changes, say to a feature gate or experiment, you'll be asked to **Submit for Review**; you can add reviewers when you submit the change for review

<img width="1168" alt="Screen Shot 2022-05-04 at 5 08 21 AM" src="https://user-images.githubusercontent.com/1315028/166678241-272adade-ca60-4942-bd04-a1413d54864c.png"/>

- Reviewers will now see an alert on the Statsig console as shown below. When they click on **View Proposed Changes**, they will see a diff of the *current version* in production and *new version*. Reviewers can now **Approve** or **Reject** the submitted changes.

<img width="871" alt="image" src="https://user-images.githubusercontent.com/1315028/166675031-43a138eb-c1ec-4272-ad51-bed66c6379b6.png"/>

![Screen Shot 2021-12-15 at 4 19 18 PM](https://user-images.githubusercontent.com/1315028/146821955-57fb8ca5-844c-45d8-8c19-280b5f196cc8.png)


### Creating Review Groups
To create a predefined group of reviewers,

- Navigate to the **Basic Settings** tab under your **Project Settings**, and click the **Create New Group** button under **Project Members and Groups** 

![Screen Shot 2022-06-27 at 8 31 24 AM](https://user-images.githubusercontent.com/74584483/175977950-01f18981-ad91-4116-ab4c-9e69a9a6de98.png)

- Enter the name and members of the group and click **Create**.  

![image](https://user-images.githubusercontent.com/1315028/146826405-0f9070f7-8aa4-4c10-8802-178bef5e1505.png)

- You can now use these predefined **Review Groups** when you submit any changes for review.

![image](https://user-images.githubusercontent.com/1315028/166684577-29598c7f-fcba-4c7e-848d-9a45b031bd79.png)

### Enforcing Team Reviews
You can _a priori_ restrict who can make changes to your Project by (a) turning on **Reviews Required** for your Project and (b) adding designated **Review Groups** or **Reviewers** when you create the Feature Gate or Experiment. 

For (a), see section **Turning on Change Reviews for a Project** to turn on project-wide reviews. For (b), as an owner of a Feature Gate or Experiment, you can add designated **Review Groups** or **Reviewers** at any time as shown below. This ensures that only these designated groups or members can review and approve any subsequent changes. When another member now tries to edit these designated review groups/reviewers, this will require approval from currently designated reviewers. 

<img width="655" alt="image" src="https://user-images.githubusercontent.com/1315028/166682283-c9e2de57-0b9a-473e-adf2-100a240ab6b0.png"/>

<img width="458" alt="Screen Shot 2022-05-04 at 5 14 57 AM" src="https://user-images.githubusercontent.com/1315028/166682177-d44411e6-c4ab-49fe-9250-c77b063621af.png"/>

### Self-approvals for Admins  
As a Project Admin, you can allow yourself and other Project Admins to self-approve review requests. To turn on this setting,
- Navigate to the **Project Settings** page
- Click on the **Edit** button next to **Config Review Requirements**
- Click the checkbox to **Allow Project Admins to self-approve reviews** as shown below

<img width="1109" alt="image" src="https://user-images.githubusercontent.com/1315028/166682645-b2daf076-7f8b-4413-9bc7-01e92e8eeb05.png"/>

### Configuring Review Settings for Different Environments 
Many teams build, test, and launch new features and experiments across multiple development environments. Statsig makes creating and using environments in feature launches easy via our [Environments support](https://docs.statsig.com/guides/using-environments#configuring-environments). 

You can also configure which environments require reviews via your **Project Settings**. To do so, go to **Project Settings** --> **Keys & Environments**  --> tap **Edit** on **Environments**. 

By default if you have turned on "Reviews Required" for your Project, reviews will be required for Production, but not non-Production (lower) environments. 

![Screen Shot 2023-04-11 at 9 47 12 AM](https://user-images.githubusercontent.com/101903926/231233087-5b87310d-b33b-456e-b1a7-7a73555c8100.png)

![Screen Shot 2023-04-11 at 9 48 02 AM](https://user-images.githubusercontent.com/101903926/231233356-967c9785-5a89-4cac-a04a-e3f11cb7bb12.png)
