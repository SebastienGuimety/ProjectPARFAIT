# [Project PARFAIT](https://sebastienguimety.github.io/ProjectPARFAIT/) 

## Installation Real Website ( https://parfait.univ-avignon.fr/ )

1. Clone the repository, place it in a folder
2. Modify the _config.yml file, replace   baseurl:  "/ProjectPARFAIT" to baseurl: ""
                                          and url:  "https://SebastienGuimety.github.io" to url: ""
3. Build your site: `bundle exec jekyll serve` , You should see a link locally after doing the command: example `"http://127.0.0.1:4000/"`
4. Once all changes are made locally, use the command :  `bundle exec jekyll build`
5. You should see a file named _site
6. Open filezilla or other software to transfer the _site folder to the virtual machine.
7. In filezilla , on the VM side , go to the folder /var/www/html/, and replace the entire file with the previously generated _site
8. Verify the change on https://parfait.univ-avignon.fr/, changes must be seen instantly, otherwise repeat the previous steps




## Installation & Setup

### Using RubyGems

When installing the theme using RubyGems, demo images, posts, and pages are not included. Follow the instructions below for complete setup.

1. Install ruby on your computer
2. Install jekyll with the command prompt : `gem install jekyll bundler`
3. Install bundler : `bundle install`
                   then `bundle init`
4. Edit GemFile ( supposed to be in /user ) with: `gem "jekyll"`                 
5. Build your site : `bundle exec jekyll serve`
6. You should see a link locally after doing the command: example `"http://127.0.0.1:4000/"`

Assuming there are no errors and the site is building properly, follow these steps next:

1. For each new post in the `_posts` directory, update the front matter. Example:

    ```markdown
    ---
    layout: post

    title: "Optimal Trunk-Reservation by Policy Learning"
    subtitle: "In Proc. of the IEEE Conference on Computer Communications (INFOCOM), Paris, France, 29 April - 2 May 2019."
    author: "A. Massaro, F. De Pellegrini and L. Maggi"
    lienofficiel: "https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8737552"
    lienhal: "(linktohal)"


    tags:
      - Optimal
      - Learning
    ---
    ```
    
2. For each new meeting in the `_meetings` directory, update the front matter. Example:

  ```markdown
    ---
    layout: post
    title:  "First Meeting"
    subtitle: "test meeting"
    author: none
    ---
  ```

6. Build your site: `bundle exec jekyll serve`
7. (Optional) Export your site locally ( build _site ):  `bundle exec jekyll build` 


## Push to GitHub 

As long as everything works locally :

1. Commit and Push the change to github
2. If github-pages is created, you will se the change on your site a few minutes later
3. If github-pages is not created on your repository, go to your github repository, you have to go to: `settings -> pages -> Source (branch : main ):  /root `
4. Save the change after that
5. A link will be given to you and your site will be online in a few minutes later
