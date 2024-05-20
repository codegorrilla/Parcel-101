## Parcel-101

#### All issues and their solutions while using parcel bundler for any type of web app development

* In case using any ES modules features, as import/export, while fetching any JS files in the HTML file use type="module" attribute in the <script> tag.
* While using any third-party JS/jQuery library, such as data tables, parcel bundler can cause issue while building, in order to resolve that we have to force clean the parcel cache, use the following code to do it and post to it either run npm start or npm run build based on your requirement.<br>
`Remove-Item -Recurse -Force .parcel-cache`

* In case of compiling multiple HTML files, use the following line of code in the package.json file as<br>
`[
    "src/index.html",
    "src/actions.html",
    "src/tables.html"
]`

* To install data tables library inside parcel build, use the following code to install data table JS library,<br>
`npm install --save datatables.net-dt`  <br> and import it inside any JS file using ES import module as  <br> `import DataTable from 'datatables.net-dt';`


