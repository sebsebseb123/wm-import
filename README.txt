====================
wmod module... needs a name change
====================
INSTALL

1. Install module just like you would any other.
1.a. NOTE: It has dependencies. So, install those too.

2. That's it for install.

====================
BASIC USE
====================

1. Go to the wmod settings page (Under the "Site Config" menu in admin menu, at:
admin/settings/wmod

2. There are no "Imports", so add one.
2.a. NOTE:TODO: There's no way to select "No Menu", as the default menu.

3. You're now back at that list of your "Imports". Click on the one you just made.

4. Now you're at the Edit page for your "Import". If you look under the "Results" group, you'll notice that "scanned = 0" and "not_scanned = 1". This is because we only have the base URL in the system right now. So, to start scanning from the base URL, click "Scan".
4.a. If your base URL has a lot of links, the scanning most likely didn't finish. It's setup to stop automatically to prevent PHP from halting the script.
4.b. After each scan, the results should update. If you like, you can keep clicking until it's 100%. But, you don't have to, you can import pages as soon as it's found any page to import.

5. Adjust the XPaths under the Node Settings group. These should be CSS style selectors to define each field.
5.a. NOTE: These are just defaults and can be changed per page.
5.b. ALSO-NOTE: If you leave a field empty, it won't try to scan or populate that field.
5.c. LAST-NOTE: During import, a title is needed... so, if the script can't find a title using your XPath, then it won't submit... but you'll get a error msg reminding you of this.

6. Click save.

7. Now you're back at the list again... kind of annoying, but click on your "Import" again. Then click on the "Import!" tab.

8. Now... you should be at a paginated list of your available links. They're organized alphabetically, to help you import "sections" of a site at a time.

9. Click a link to open it...
9.a. NOTE: If you see the base URL in this list... I don't think you can import it yet... I was having trouble with that one before... but pick any other one.

10. Click preview to fetch the data. Did it work? Are you seeing blank fields? If so, read on...
10.a. If the data isn't showing up, it's probably the XPaths. Click on "Settings" under that link. You can adjust them there.
10.b. Not sure what the XPath is? There's a link, labeled "Link: ". You can click on that to view the page... now you can use firebug or similar to find the XPath!

11. Everything looks good? Great! Click "Save"
11.a. NOTE: Ignore the numbers in the buttons...
11.b. NOTE: You must preview before you save... it actually uses the previewed data to submit the node...instead of fetching it again.
11.c. NOTE: If there are images in the body, they've automatically been downloaded to your drupal install upon preview... also the <img src="" urls have been updated accordingly. 
11.d. NOTE: Not all cck fields are supported just yet... but the basic ones are.

12. That's it... now you can have different "Imports" to bring different sites into your one site. 

====================
TODO
====================

- Add more cck support
- Add "No Menu" support
- Verify content_fields better
- Add "extend PHP timeout limit" setting
- Add "Blind Import" button
- Add "Imported" field to url table
- Add "Blind Import Page" button
- Add "Blind Import All" button

