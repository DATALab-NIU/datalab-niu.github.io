# DATALab Website
<img src="assets/images/datalab-logo-horizontal.png" alt="DATALab" width="300"/>

Welcome to the DATALab website! This site is built using [Jekyll](https://jekyllrb.com/), a static site generator, and is hosted on [GitHub Pages](https://pages.github.com/). Below you'll find instructions on how to set up your local development environment, contribute to the site, and deploy changes.

## Prerequisites
For local development, you'll need to satisfy Jekyll's prerequisites [listed here](https://jekyllrb.com/docs/installation/#requirements).
It is also possible to update content without local installation. Local jekyll setup is only needed if you want to preview changes before pushing them to GitHub. Please note that basic [Markdown](https://www.markdownguide.org/basic-syntax/) knowledge is required to edit the content.

## Local Development Setup
1. **Clone the Repository**: Start by cloning the `website-publish` branch from the GitHub repository to your local machine.
2. **Install Jekyll and Bundler**: If you haven't already, install Jekyll and Bundler using the following command:
   ```
   gem install jekyll bundler
   ```
3. **Install Dependencies**: Navigate to the project directory and run:
   ```
   bundle install
   ```
4. **Serve the Site**: To build and serve the site locally, use:
   ```
   bundle exec jekyll serve
   ```
   This will start a local server, and you can view the site in your browser at `http://localhost:4000`.
5. **Make Changes**: Edit the Markdown files in the `_members` directory to update member profiles or other content as needed.
6. **Preview Changes**: As you make changes, Jekyll will automatically rebuild the site. Refresh your browser to see the updates.
7. **Stop the Server**: When you're done, you can stop the server by pressing `CTRL + C` in the terminal.
8. **Commit and Push Changes**: After verifying your changes, commit them to your local repository and push them to the remote repository on GitHub. Please create a **new branch** for your changes and open a pull request to the `website-dev` branch.
9. **Merge Changes**: Once your pull request is reviewed and approved, it can be merged into the `main` branch. GitHub Pages will automatically rebuild and deploy the site. You may need to contact site administrators at [ashiqur.r@niu.edu](mailto:ashiqur.r@niu.edu) or [alhoori@niu.edu](mailto:alhoori@niu.edu) to trigger a rebuild if necessary.

If you do not want to set up a local development environment, you can ignore steps 2-4 and steps 6-7. You can directly edit the markdown files in the GitHub web interface and create a pull request for your changes. <span style="color: red;">**_It is imperative that you don't make any changes directly to the `website-publish` branch._**</span> Please create a new branch for your changes and open a pull request to the `website-publish` branch. Once your pull request is reviewed and approved, it can be merged into the `website-publish` branch. GitHub Pages will automatically rebuild and deploy the site.

## Contributing
There are several ways you can contribute to the DATALab website. Most importantly, you should keep your own profile and publications up to date.

### Updating Your Profile
To update your profile, locate your Markdown file in the `_members` directory. The file should be named in the format `lastname_firstname_degree.md`. For example, if your name is John Doe and you are a PhD candidate, your file should be named `doe_john_phd.md`. If you cannot find your file in the `_members` directory, you can create a new file with the same naming convention. Please duplicate the sample file `_members/lastname_firstname_ms.md` or `_members/lastname_firstname_phd.md` and fill in your details. Make sure to rename the duplicated file to match your name and degree. Here are some key fields to update:
- `layout`: This should always be set to `member`. Do not change this.
- `title`: The title of your profile, which will be used in the browser title bar and for SEO.
- `full_name`: Your full name.
- `level`: Your academic level (e.g., Faculty, PhD, MS, BS).
- `position`: Your current position or role (e.g. Research Assistant, Social Media Coordinator, etc.).
- `order`: A number to order the profiles correctly. Faculty=1, PhD=2, MS=3, BS=4. You should not change this number.
- `hidden`: Set this to `true` if you want to hide your profile from the members page. This is useful if you are not currently active in the lab or if you prefer not to have your profile displayed.
- `picture`: The path to your profile picture. Place your image in the `assets/images/members/` directory and update the path accordingly. Make sure not to replace any existing images, as they may be used by other members. If you do not have a profile picture. You can also provide a link to external image hosting services like [Gravatar](https://gravatar.com/) or [Imgur](https://imgur.com/). However, external images may not be as reliable as hosting them directly in the repository. Please upload an square image with at least `512x512` pixels resolution.
- `bio`: A short description of your profile. This should be a brief overview of your academic and professional background. No more than 1-2 sentences.
- `email and other social media links`: Update these fields with your contact information and social media profiles. If you do not have a specific profile, you should remove it from the file.
- `Biography`: This section should contain a more detailed biography of your academic and professional background. You can use Markdown syntax to format the text.
- `Publications`: List your publications in the format provided in the sample file. Order the items by year, with the most recent publication first. Use the format:
  ```
  - **Author(s)**. (Year). Title of the publication. *Journal Name*, *Volume*(Issue), Page range. DOI or URL
  ```
  If you do not have any publications, you can remove this section.

### Updating Publications
When you have a new publication, we can feature it on the publications page of the website. Besides adding the publication to your profile page, you should update the `pages/publications.markdown` file. This file contains a list of all publications from the DATALab team. You should add your publication to the appropriate year section, following the same format as in your profile page. Make sure to order the publications by year, with the most recent publication first.

### Adding News/Updates
To add news or updates to the website, you can create a new Markdown file in the `_posts` directory. The file should be named in the format `YYYY-MM-DD-title.md`, where `YYYY-MM-DD` is the date of the post and `title` is a short description of the post. For example, `2025-01-01-new-year-update.md`. In the file, you can use Markdown syntax to format the content. The posts will be displayed on the homepage and the about page of the website.
