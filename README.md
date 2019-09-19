# Multi-Contact-Creation-View-with-Pagination

#### A visualforce page which has 2 sections. First section have an option to create multiple contacts at a time.When contacts are saved in the first section, they get displayed in the second section. In the second section I have also implement pagination for easy navigation.

Code Walkthrough: In this functionality I am using 2 pageBlockTable to showcase
contact fields in a Tabular format, one is for adding Contacts and other one is for
showing Contacts. When our apex class constructor is called, I am adding a new Contact
object in the Add Contact List with no data so that when our UI gets rendered it will
show a blank record in First Section pageBlockTable. When someone clicks on Add
Contacts it adds another Contact object with no data in the List and refreshes the page.
This way our UI shows 2 records. When someone clicks on save, I am inserting all the
data in the database in one go and renders the second pageBlock which will showcase
all inserted Contacts. I have used custom logic to achieve pagination functionality. In UI I
am showing Page Numbers commandLinks, on click of that I am calling apex
actionFunction which reads the value of clicked commandLink and set the value in our
apex class variable and calls the apex method. In that method I am checking for the
range that need to be visible in UI on the basis of selection and based on that I am
filtering data from the List and refreshes the UI.
