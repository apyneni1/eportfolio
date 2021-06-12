## Welcome to Aparna Pyneni ePortfolio (Course ID:CS-499)!!!

### Professional Self-Assessment:

This section will be updated next week 


### Enhancement One: Software Design and Engineering
Enhanced the “Wellness Tracker” Android mobile application for better software design and engineering practices. The enhancements included avoiding the duplicate usernames and increase the password criteria etc. Full write-up on the code enhancement can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/3.2%20Milestone%20Two%20Narrative.docx).

Following are the code enhancement snippets and full code can be downloaded by [clicking here](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/3.2%20Milestone%20Two%20Narrative.docx).
```
 if (!uname.isEmpty()){
      boolean IsUsernameTaken = myDB.UsernameExists(uname);
      if (!IsUsernameTaken && !pwd.isEmpty() && pwd.length() >6) {
           boolean isInserted = myDB.insertUser(uname, pwd);

public boolean UsernameExists(String name) {
        SQLiteDatabase db = this.getWritableDatabase();
        String[] columns = {"Username"};
        String selection = "Username=? COLLATE NOCASE";
        String[] selectionArgs = {name};

        Cursor cur = db.query(WeightTables.TABLE1, columns, selection, selectionArgs, null, null, null);
        int count = cur.getCount();
        if(count > 0)
            return true;
        else
            return false;
    }
```


- [Enhanced Artifact](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/3.2%20Milestone%20Two%20Narrative.docx)
- [Enhancements Narrative](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/MyApplication.zip)

### Enhancement Two: Algorithms and Data Structure

- [Enhanced Artifact](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/4.2%20Narrative.docx)
- [Enhancements Narrative](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/4.2%20Security%20Policy.docx)

### Enhancement Three: Databases 

- [Enhanced Artifact](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/5.2%20Narrative.docx)
- [Enhancements Narrative](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/queries.txt)

You can use the [editor on GitHub](https://github.com/apyneni1/eportfolio/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/apyneni1/eportfolio/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
