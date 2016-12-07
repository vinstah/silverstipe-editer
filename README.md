# silverstipe-editer
SilverStripe CMS demo inline-edit
Silverstripe 3.6+ SilverStripe CMS 3.6+

## Templating in CMS
- Current way to edit in CMS can be time consuming, for example; Contact info is either in top level parent page or Settings module, you edit it in a form element then save and refresh the front end to see the updates. Sure this sounds easy enough, what about other data you need to change? you may have a large site with plenty of form elements to go through, in tabs etc.
- Why not edit in the front end? I know, do we really need another front end editing module? Well this one will be different, it will use the CMS because without it we wouldn't have SilverStripe.

### Vision
- Content author views a page to edit in the CMS, using the demo view of the page open the template view completely so no form fields are visable.
- Mouse over parts of the web page that are editable, which will highlight the surounding <div></div> and show a edit and save buttons.
- Once edited, the save button will become available and JS will send the new data to the API and update the DataObject to complete the request and thus edited in the CMS becomes unambiguous.

#### The workings
- In template you must add sections to edit wrapped in <div data-editable="FieldName"></div>
- JS will check for the data-editable and replace it with editable=true, then show the edit buttons when you hover over editable attributes.


