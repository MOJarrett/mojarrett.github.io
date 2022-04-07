---
layout: post
title:  "Part 1 - Building a Free Website with Jekyll and Github"
author: MJarrett
categories: [ Jekyll,Github,Ruby ]
image: assets/images/css_jquery_book.jpg
featured: true
comments: false
---
The website you are currently using was built and is being hosted completely for free. It also was very easy to build by utilising and amending existing templates. 

The widely used version control tool Github offers a free hosting service when you use your github username appended with github.io - `USERNAME.github.io`. Simply 'fork' an existing repository and use that to build your website from. I forked and amended <a href="https://github.com/wowthemesnet/mediumish-theme-jekyll" target="_blank">this repository</a>. 

Most of the repsitories I looked at were under various open source licenses which do have some conditions worth checking out. Some Jekyll themes require payment but these won't be needed unless you are doing something very advanced. I would suggest starting out with a simple one first. 

Here are the steps to follow if you want to do the same:

<ol>
  <li>Go to the chosen jekyll theme. You can browse and demo the themes <a href="https://jamstackthemes.dev/ssg/jekyll/" target="_blank">here</a>. I recommend using <a href="https://github.com/wowthemesnet/mediumish-theme-jekyll" target="_blank">this repository</a> for following this guide. Once you have found a good one you need to navigate to the github repository which can be found through links on the theme.</li>
<p></p>
  <li>Once opened in github select fork. If you don't have a personal GitHub account you will need to create one.</li>
<p></p>
  <li>Once the theme is forked you will have a new repository created which has all the files that the them uses.</li>
<p></p>
  <li>Now you should go to settings and rename the repository inserting your username in the following - 'USERNAME.github.io'. Click the rename button to confirm the change.</li>
  <p></p>
  <li>After a few minutes you should be able to enter the site name into your web browser address bar and find - e.g. enter 'USERNAME.github.io' into browser.</li>
  <p></p>
  <li>Get the application 'Visual Studio Code' downloaded on your device. These will be needed to make customising the code.</li>
    <p></p>
      <li>Copy the URL link to your Github repository shown in your web browser address bar. Open 'Visual Studio Code' and navigate to source control. Enter the URL link and click enter. Save the repository files somewhere on your device. I use a folder in documents called Github.</li>
    <p></p>
      <li>Now you can see the files from your new repository in 'Visual Studio Code' under the Explorer Tab. These are the files you will amend to customise the website for your needs.</li>
</ol>

Now you have a repository stored on your local device which you can alter. When you are happy with the changes they can be merged back to your GitHub respository. For now we can amend them locally. 

One useful tool is having being able to locally host the local repository so you can see the amendments you make as you go. This will mean you can see the changes on your browser but nobody else can. 

Open your 'Visual Studio Code' app and navigate to the explorer tab again. Find the _config.yml document. Double click to open it - it should open a tab. Now select from the app dropdowns 'View' and then 'Terminal'. Within the terminal enter the following commands and click enter after each.

<ol>
  <li>
`brew install ruby export GEM_HOME="$HOME/.gem" gem install rails`
</li>
<p></p>
<li>
`gem install bundler` installs the bundler gem through RubyGems. You only need to install it once - not every time you create a new Jekyll project.
</li>
<p></p>
<li>
Run `bundle exec jekyll serve`, `Bundler` uses the gems and versions as specified in `Gemfile.lock` to ensure your Jekyll site builds with no compatibility or dependency conflicts.
</li>
<p></p>
<li>
You should now see a message in the terminal saying a server address has been generated. Take the server address and post it into your browser. You should see the default theme you copied.
</li>
<p></p>
<li>
Now make your first change to the repository within Visual Studio Code. Create a new folder called _drafts. Find the _posts folder. We are going to drag and drop all the files from _posts into the _drafts folder. Now do a file save. You should see the jekyll feed reruns. 
</li>
<p></p>
<li>
Now when you go on the locally hosted site you will see your changes have taken effect. 
</li>
</ol>

Finally, lets push the changes you made to github. Select the source control area in VS Code which is indicated by the image shown below. You should see the number of changes you made are in a blue number. In that section you can review and changes made before commiting them. Enter a message that describes the changes you made and then whatever prompt the input box showed before you started typing (cmd+enter on mac). You should see the bottom left of VS Code show a symbol with a 1 in. 

<img src="/post_images/github_vscode.png">

Your changes should now be pushed to the main github repository. Now you can view your `USERNAME.github.io` link which is publically accesible. You should see the changes you have made are now freely visible. 

Hopefully you can see how we have created a free website which you can easily amend on your local device before pushing the changes out more widely to the world. 

In the next guides we will be exploring how to add new posts, create categories and list yourself as an author as well as further customisation. 