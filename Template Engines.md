Up:[[Node JS]] [[Python]]

# Template Engine
 Template Engines are used to display dynamically generated content on a web page. They replace the variables inside a template file with actual values and display these values to the client (i.e. a user opening a page through their browser). 
 
 For instance, if a developer needs to create a user profile page, which will contain Usernames, Emails, Birthdays and various other content, that is very hard if not impossible to achieve for multiple different users with a static HTML page. The template engine would be used here, along a static "template" that contains the basic structure of the profile page, which would then manually fill in the user information and display it to the user. 
 
 Template Engines, like all software, are prone to vulnerabilities. The vulnerability that we will be focusing on today is called [[Server Side Template Injection (SSTI)]].
  