### Method 1: easiest, all in the browser

Open your GitHub CRM repo.

Create a new branch for the change. Name it something like mobile-fix or contacts-fix.

Open the file you want to replace, like index.html.

Click the pencil/edit button in GitHub’s file view to edit it directly in the browser. GitHub supports editing files right in the repo UI.
Paste in the updated code.

Click Commit changes...

Make sure you are committing to your new branch, not main.

Save the commit with a message like Fix mobile zoom issue.

Open a Pull Request from that branch into main.

Netlify will automatically generate a Deploy Preview for that pull request on the connected site. By default, Netlify builds Deploy Previews when you open a pull request in a connected GitHub repo.


### At that point:


you test the preview link

nothing is live yet

production does not change until you merge the PR into main

How to find the preview link


## Usually one of these happens:


Netlify posts the preview in the PR checks/status

or the preview URL looks like deploy-preview-XX--yoursitename.netlify.app for PR number XX. Netlify documents that Deploy Preview URLs use the deploy-preview-<PR#>-- format.

When it goes live


It only goes live when you merge the pull request into main. Deploy Previews are for review; production comes from your production branch.


### What not to do:

Do not commit straight to main if you only want a preview.

Do not manually drag and drop to Netlify for every test if you want to avoid production deploy behavior.

Do not delete the old file from the repo first unless you are actually removing it. Just open the file and replace its contents in the editor, then commit that change. GitHub supports direct file editing and committing in place.

###### Example exact flow


### Say you want me to fix index.html:


Open repo

Create branch sidebar-status-fix

Open index.html

Click edit

Replace old code with the code I gave you

Click Commit changes

Commit to sidebar-status-fix

Click Compare & pull request

Open the PR

Wait for Netlify preview

Test preview URL

Merge only if good

