<h1>Class1</h1>


<h2>CI CD </h2>

The main concepts attributed to CI/CD are continuous integration, continuous delivery, and continuous deployment.

<h2> Invite team member</h2>

   1) click "contributer" to add your team member
   2) then click on "setting"
   3) click top left side "manage access"
   4) click invite  a  collaborators 
   5) search name of member then send invite link

<h2>download node js and install Surge</h2>

   1)open terminal and type "npm install surge"

   Note:it is available only for your one folder or project


   2)open terminal and type "npm install -g surge" or "npm install --global surge"

   Note:Both command doing same work first one is just for shortcut -g or --global is use for your all repository or you will use in your all project


<h2>Deployment</h2>

1)open terminal type surge
2)Enter your domain like "class1.surge.sh"
3)open in google


<h2>Git Workflow Action</h2>

1)Click on Action
2)Then click set up a workflow yourself 
3)Create a Action & Create a Secret type "surge token" in terminal and create secert put the value of your secret in last line under bracket 

    - name: Installing Node
      uses: actions/setup-node@v2-beta
      with:
        node-version: 12

    - name: Installing surge
      run: npm install --global surge
    - name: deploying using surge
      run: surge ./ waiting-system.surge.sh --token ${{ secrets.SURGE_TOKEN }}
