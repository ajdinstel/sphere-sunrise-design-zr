- Always work with Pull Requests when working with the template (this is extremely important when touching any JSON file). Otherwise the work cannot be reviewed properly, thus fixing wrong stuff becomes complicated.

- Always mention `@lauraluiz` in the PR when modifying some .hbs or .json file, so it can be reviewed and validated, and to be aware of how this will affect the backend side too.

- Do not modify JSON files unless we all agree on that (extending is okay, as long as it is reviewed). The JSON files is the contract between the template and all the shops using it, so it cannot be changed lightly.
 
- When extending a JSON file, consider putting all common stuff (`header`, `footer`, `meta`) in root level and inside `content` any page-specific data. This is a good way to avoid name collisions in the future.

- In the JSON files, field names should be only alphabetical characters (no other symbols such us `-`, `_`, `.`) otherwise it can be a source of problems for the applications using the template. For example, "banner mobile" should be named "bannerMobile".
 
- Never create a page index.html (or index.hbs). It can be useful to have a index.html in GitHub Pages in the future, so let's better reserve it.
