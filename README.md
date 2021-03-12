---
title: Listing your Project
description: How you can list your TestNet project or dApp on the Moonbeam documentation site
---

# How to List your Project/dApp

![Template banner image](images/list-dapps-banner.png)

**Disclaimer:** Moonbeam is a permissionless network. Any project can deploy its contracts to Moonbeam. The content in this section is entirely community-managed.

## Minimum Content

In general, to be considered and added to this list, your project/dApp must meet the following requirements in terms of content:

 - Introduction (see template file)
 - Show working contracts and/or front-ends deployed or connected to the Moonbase Alpha TestNet
 - Explain to users how they can test or integrate your project/dApp
 - Link the GitHub repos of the code
 - Link to communication channels

## Getting Started

This guide will help you get started on listing your project/dApp in the Moonbeam docs site.

### Forking/Cloning the Repo

The main idea is to fork a repository, modify it with your changes, and then submit a PR.

So, as mentioned before, first fork [this repository](https://github.com/PureStake/moonbeam-project-directory).

### Choose Category and Copy Template

Next, choose the category that relates to your project the most. There is a folder per category. If you think we are missing a category, contact us via our [Discord channel](https://discord.gg/PfpUATX), we are happy to add it to the list.

Inside each category, there is an `example.md` file. You can use it as a reference.

For example, let's say your project is named "Rocket Project" and related to DeFi. Then, you would need to copy this file inside the following folder:

```
moonbeam-project-directory
|--apis
|--assets
|--bridges
|--defi
|--|--example.md
|--|--rocket-project.md
|--explorers
...
```

### Changing Title - Description - First Heading

With the file in the correct location, you can start adapting it to your specifications. Make sure to change the title, description, and first heading (all located at the top of the file). The title defines how the entry is named on the left-hand side navigation menu. The description is related to the metadata of the page:

```
---
title: Rocket Project (title example)
description: Rocket Project DeFi integration in Moonbase Alpha to access the Multi-Chain future and the Polkadot Ecosystem (description example)
---

# Rocket Project - DeFi Multi Chain (title example)
```

### Images

Images related to your documentation can be saved inside the `images` folder, located in the repo's main directory. Please create a folder where to save your images. For our previous example, this would be in:

```
moonbeam-project-directory
|--apis
...
|--defi
|--explorers
|--images
|--|--rocket-project
|--|--|--image1.png
|--|--|--image2.svg
|--marketplaces
...
```

## Submitting PR

Once you are done with your documentation, you can submit your pull-request from your forked repo.

Our team will check this PR to make sure it complies with the minimum requirements to be listed.
