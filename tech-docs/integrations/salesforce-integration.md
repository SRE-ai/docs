---
description: Learn how to set up SRE.ai in your Salesforce Workspace.
---

# Salesforce integration

## Install SRE managed package in Salesforce Workspace

The Salesforce environment connected to the workspace **acts as a remote connection for storing and synchronizing metadata** from the SRE.ai Application with other team members and application nodes.

### Installing the managed package

1. Log in to your Salesforce environment
2. Use the following link to install the managed package

```javascript
/packagingSetupUI/ipLanding.app?apvId=04taj0000006Gi1AAE
```

3. Click **Install for Admins Only**
4. Click **Install**

### Ensure functionality

{% hint style="danger" %}
New users must verify their email address in the Salesforce user record before being granted access.
{% endhint %}

After installation, grant SRE users permission to access **objects, classes, and other components.**\
\
This step is required for functionality to work as expected.

{% hint style="success" %}
Please ignore the warning. We are working through the Security Review for the AppExchange Partner Program.
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfj64wUQtS3FoKiZjgIt0cqyZX8MGeWtMbZXoxoqYzeJ6VVxNGF3ntI0mfjE9nZqbvqk9P768WGEyXrwTgbP0PE7PpUl-nGsdMskhG4_0-p7dj5Jue7wAvW2pEZoV8HOK35_7jd?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

## Create a connected app in your org for GitHub actions

Salesforce CLI requires a connected app in the org that you're authorizing.\
\
A connected app will enable you to integrate Salesforce CLI with Salesforce using APIs and standard protocols, such as OAuth.

### Download JWT certificate

1. Go to the [SRE App](https://ramp.sre.ai/)
2. Select **Settings** from the **User menu** option on the top-right

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdo-LJ5jA_HbkALZ5x6LXPsGNoeQGmKsx6qcl35G0f9UPG7kTof89vwPEtkGFlHwtPEpHecV3_PjdfPkRRjxfINTBuQkF9CAY_hvKScw5rH6q_e2pV29HRRx7NCrrXH-E1xDQoORQ?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

3. Select the **Certificate** tab under **Settings**
4. Click **Generate New** to download a certificate necessary for creating a connected app.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfETZ7_w4RTkMfl01qbvQYGF5KPVqknAwGDXzK9Qc0TmRSqd-66zu0Ei7J571C-9Pj41z4dOiAzkoy1ZsKeA025KWYi-jeSYDwZWrf7SYHio08o9CCH0wZPB3T-BQsE9umBekDwQg?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

### Create a Connected App

1. Go to **Salesforce Setup**
2. Search for **App Manager** in the quick-find&#x20;
3. Click **New Connected App**
4. Select **Create a Connected App** in the dialog
5. Click **Continue**
6. Adjust the following settings (modify as needed):
   1. **Connected App Name**: GitHub Action JWT
   2. **API Name**: GitHub\_Action\_JWT
   3. **Contact Email**: \<Administrator Email>
   4. **Enable OAuth Settings**: Checked (Checkbox)
   5. **Callback URL**: [http://localhost:1717/OauthRedirect](http://localhost:1717/OauthRedirect)
   6. **Use digital signatures**: Checked (Checkbox)
7. Upload the Certificate from [the previous step](salesforce-integration.md#download-certificate)
8. Select the following OAuth Scopes:
   1. **Access the identity URL service** (id, profile, email, address, phone)
   2. **Full acces**s (full)
   3. **Manage user data via APIs** (API)
   4. **Manage user data via Web browsers** (web)
   5. **Perform requests at any time** (refresh\_token, offline\_access)
9. Adjust the following settings:&#x20;
   1. **Require Proof Key for Code Exchange (PKCE) Extension for Supported Authorization Flows**: Un-checked (Checkbox)
   2. **Require Secret for Web Server Flow**: Checked (Checkbox)
   3. **Require Secret for Refresh Token Flow**: Checked (Checkbox)
10. Click Save

### Update Permitted Users

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHvpvfCzC9KHI_7ZBy9NDWjShBw8UVvE0BsXnsLuyUBjaqHEAcAr-zi7lzV7M5Gz4D38G0L6vk4CvllQJlo54c5crNhL1ftT0gxhgFDJxxDj8VOwgQK5PLNJdOKQCsj6yEItoCqA?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

1. Click **Manage**
2. Click **Edit Policies** and update **Permitted Users** to **Admin approved users are pre-authorized**
3. Click **Save**
4. Click **Manage Profiles**
5. Include the **System Administrator Profile** in the **Profiles** section

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfWUpm9zM5otJ2EHjeJ9Q8q7C0th3ehbLgxDL1gy72D_Td2KJv902sZFL5mSyG7Z0qALpUTOWo4sRYWM8xJ7PN3IvyBGAFHxICe_HVfmN4gqe8B4llH_Sq8eCZ-iUmb4SLXw_dytg?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

6. Click **Manage Consumer Details**
7. Take note of the **Client ID** and **Client Secret**

***

## Install GitHub app to ramp GitHub workspace

1. Add our AlphaSRE app to your GitHub Repository using the following link: [https://github.com/apps/alphasre](https://github.com/apps/alphasre)
2. Share the **Installation ID** with the SRE.ai team:
   1. Select the **GitHub Repository Settings**
   2. Click **GitHub Apps**&#x20;
   3. Click **AlphaSre Configure**
3. Copy the **Installation ID** in the URL

```javascript
https://github.com/ACME/CRM/settings/installations/<installation id>
```

## Setting up GitHub Action Secrets and Variables

1. Select the **GitHub Repository Settings**
2. Click **Actions** under **Secrets and Variables** on the left menu
3. Add the following Secrets and Variables:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcir755TUyGCE_hJH5-pJNg9HTg-2KIolM6QmBMgGj2CZoGYuNOBSayPS_vJpP7Lm34pE0GzLO6MjLXeF2sbVcZX6AN7AbFi86gczF035LhqR8uiuYMA2nU3uPiBR-JS3YOCsd2PA?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

### Secret 1:

Name: SRE\_KEY

```
BASE64 Encoded Key for Certificate generated in Previous Step- Create a Connected App in Your Org for GitHub Actions > Step 3
```

### Secret 2:

Name: SRE\_WORKSPACE\_CLIENT\_ID

```
Client Id for GitHub Action JWT
```

### Secret 3:

Name: SRE\_WORKSPACE\_USERNAME

```
Value: User’s Username

```

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfv-ZTp-KKJhecUjVzPUlm_867aG9F8jj1_9TKtHqV-cuXJZHj4EEoX9FDMXxhN9X3x_Nh7465YE_Bpitv4FF44FB3--qavsXlXZP46CFtgbkgbQjVKKVp6MDeaxLL2j2umVNEs1g?key=DkBAADFS-Ge2WW_jAdqd55hX" alt=""><figcaption></figcaption></figure>

### Variable 1:

Name: SRE\_TEAM

Value: RAMP

### Variable 2:

Name: SRE\_USERNAME

Value: \<User’s Email ID>

## GitHub Action YAML

Include the following YAML file in your repository to bind the Pull Request Approval and the Label to perform Continuous Deployment for file location _**.github/workflows/AlphaSRE CI Agent.yml**_

```
name: AlphaSRE CI Agent

on:
  pull_request_review:
    types: [ submitted ]
  pull_request:
    types: [ labeled ]

jobs:
  promote_to_stage:
    name: Promote to Stage
    if: github.event.pull_request.base.ref == 'stage' && ( github.event.review.state == 'approved' || contains(github.event.pull_request.labels.*.name, 'Skip-Reviews') )
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - name: Checkout 
        uses: actions/checkout@v4
      - name: AlphaSRE Agent GitHub Action
        uses: SRE-ai/sre-github-action@v0.1
        with:
          image: sreai/platform:latest
          options: -v ${{github.workspace}}:/usr/src/app/docs/sre/data/ramp/git/ramp-tryout -e SRE_TEAM=${{vars.SRE_TEAM}} -e SRE_USERNAME=${{vars.SRE_USERNAME}}
          run: |
            git config --global --add safe.directory /usr/src/app/docs/sre/data/ramp/git/ramp-tryout
            git config --global user.email "${{vars.SRE_USERNAME}}"
            git config --global user.name "${{vars.SRE_USERNAME}}"
            sh sre.sh configure -k "${{secrets.SRE_KEY}}"
            sh sre.sh authorize -u "${{secrets.SRE_WORKSPACE_USERNAME}}" -k "${{secrets.SRE_WORKSPACE_CLIENT_ID}}"
            sh sre.sh promote -b "${{github.event.pull_request.head.ref}}" -i "stage" -r "ramp-tryout"

  promote_to_prod:
    needs: promote_to_stage
    name: Promote to Prod
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - name: Checkout 
        uses: actions/checkout@v4
      - name: AlphaSRE Agent GitHub Action
        uses: SRE-ai/sre-github-action@v0.1
        with:
          image: sreai/platform:latest
          options: -v ${{github.workspace}}:/usr/src/app/docs/sre/data/ramp/git/ramp-tryout -e SRE_TEAM=${{vars.SRE_TEAM}} -e SRE_USERNAME=${{vars.SRE_USERNAME}}
          run: |
            git config --global --add safe.directory /usr/src/app/docs/sre/data/ramp/git/ramp-tryout
            git config --global user.email "${{vars.SRE_USERNAME}}"
            git config --global user.name "${{vars.SRE_USERNAME}}"
            sh sre.sh configure -k "${{secrets.SRE_KEY}}"
            sh sre.sh authorize -u "${{secrets.SRE_WORKSPACE_USERNAME}}" -k "${{secrets.SRE_WORKSPACE_CLIENT_ID}}"
            sh sre.sh promote -b "${{github.event.pull_request.head.ref}}" -i "prod" -r "ramp-tryout"

```

## Create a Connected App in Your Org for SSO

The SRE Application can now use your Salesforce Org as an Identity Provider and, by default, inherits its SSO capabilities.

1. Go to **Salesforce Setup**
2. Search for **App Manager** in the quick-find&#x20;
3. Click **New Connected App**
4. Select **Create a Connected App** in the dialog
5. Click **Continue**
6. Adjust the following settings (modify as needed):
   1. **Connected App Name**: GitHub Action JWT
   2. **API Name**: GitHub\_Action\_JWT
   3. **Contact Email**: \<Administrator Email>
   4. **Enable OAuth Settings**: Checked (Checkbox)
   5. **Callback URL**: [http://localhost:1717/OauthRedirect](http://localhost:1717/OauthRedirect)
   6. **Use digital signatures**: Checked (Checkbox)
7. Upload the Certificate from [the previous step](salesforce-integration.md#download-certificate)
8. Select the following OAuth Scopes:
   1. **Access the identity URL service** (id, profile, email, address, phone)
   2. **Full acces**s (full)
   3. **Manage user data via APIs** (API)
   4. **Manage user data via Web browsers** (web)
   5. **Perform requests at any time** (refresh\_token, offline\_access)
9. Adjust the following settings:&#x20;
   1. **Require Proof Key for Code Exchange (PKCE) Extension for Supported Authorization Flows**: Un-checked (Checkbox)
   2. **Require Secret for Web Server Flow**: Checked (Checkbox)
   3. **Require Secret for Refresh Token Flow**: Checked (Checkbox)
10. Click **Save**
