-
- DOING [Title](URL)
  id:: 67039ad1-e54a-4a1f-9efa-4649e2c052a0
  collapsed:: true
  :LOGBOOK:
  CLOCK: [2024-10-07 Mon 15:25:01]--[2024-10-07 Mon 15:25:02] =>  00:00:01
  CLOCK: [2024-10-07 Mon 15:25:02]
  :END:
	- When use this plugin in a page, it works.
	  But when click a block  then enter into a single "page"(in fact it not a page), then use this plugin to repalce some word, it don't work.
	  So how use in a block "page"?
- TODO [Title](URL)
  id:: 67039ad1-b3e7-4791-919e-3f3d6d623335
  collapsed:: true
	- Hide Brackets option only hides [[links]], but not the custom text ones `[text](links)`.
	  `[text]([[links]])` gets turned into `[text](links)`
- TODO [Title](URL)
  id:: 67039ad1-d230-4c9e-8bc6-2c60ee4feb58
  collapsed:: true
	- This patch adds a new feature that adds a reference of the block that links were produced for into the pages that were found. A new setting is added for it called `referenceInPages` and is disabled by default. Tests were also modified as the pages found needed to be returned from the `replaceContentWithPageLinks` function.
- TODO [Title](URL)
  id:: 67039ad1-72ad-4091-9467-4824a331adfa
  collapsed:: true
	- I have used this plugin for 3 months now, everything good, except that this plugin also links to tags, which, compared with page blocks, are more commonly used words and may result in many unwanted links.
	  It would be great if there is way to toggle whether to ignore tags.
	  Thank you, developer, keep up the good work!
- TODO [Title](URL)
  id:: 67039ad2-7c1d-4deb-b1df-5f76dd1602c6
  collapsed:: true
	- I use dark mode for editing, but I don't want the PDF to use that theme. If I switch to light theme first before printing to PDF, I can get the result I want, but it would be nice not to need to do that.
- TODO [Title](URL)
  id:: 67039ad2-d6fe-44f0-9d75-f3dbc4a0a10e
  collapsed:: true
	- Hi,
	  thanks for your work on the plugin! However, I have some troubles using it properly. My tags are only recognized if they already exist prior to writing a sentence / block. I assume this is not the intended behavior. Please tell me if I can provide additional debugging data (e.g. JS) to check the origin of the problem. Or is it just misconfiguration?
	  
	  
	  https://github.com/user-attachments/assets/842d2b68-5577-4ef7-8dff-5c95d003a040
- TODO [Title](URL)
  id:: 67039ad2-471a-492f-bd49-158eaddbbe4d
  collapsed:: true
	- ### Original Issue: [Linker parsing property blocks #28](https://github.com/sawhney17/logseq-automatic-linker/issues/28)
	  #### Details:
	  **Sep 23, 2022**
	  > Having the "autocomplete on Enter" on, the linker parses property blocks and tries to link them.
	  > This corrupts the syntax and throws a parsing exception for the block.
	  > E.g., type:: page becomes [[type]]:: [[page]]
	  
	  **Sep 24, 2022 - @andreoliwa's [response](https://github.com/sawhney17/logseq-automatic-linker/issues/28#issuecomment-1257068986)**:
	  > Hi, this should have been fixed by #29. The new release made today includes the fix: https://github.com/sawhney17/logseq-automatic-linker/releases/tag/1.3.0
	  ---
	  ### Update 2024-07-18
	  
	  According to the information above, this issue should have been resolved by #29 however, it does not appear that this issue has truly been resolved. It may have been previously, but it appears that this behavior is still present. I have only tested this issue with the `alias::` and `title::` properties but I am assuming this applies to any and all page properties, but I have not specifically tested any others. The impact on these two properties alone is enough for it to be a breaking issue for me.
	  
	  ### Example:
	  
	  When attempting to create a new page called "mobile version" with the following properties:
	  > alias:: mobile versions, mobile version's, mobile versions', mobile-version, mobile-versions
	  > title:: mobile version
	  > > ![image](https://github.com/user-attachments/assets/cc581ff1-cb50-4b5e-9c43-d57f7eb5d965)
	  
	  Upon pressing `Enter` key, the auto-linker plugin parses the page title and the alias values into page references. #29
	  > alias:: mobile [[versions]], [[mobile [[version]]]]'s, [[mobile]] [[versions']], mobile-version, mobile-versions
	  > title:: mobile [[version]]
	  > > ![image](https://github.com/user-attachments/assets/d2727028-4fbc-4ee6-996b-919451250de7)
	  
	  Any aliases affected by this do not work as intended. 
	  For example, the alias, "mobile versions", that I attempted to add, became "mobile [[versions]]". As a result, when I try to create a page reference to "mobile versions" using "[[mobile versions]]", it attempts to creates a new page, because it does not recognize it as an alias of the "mobile version" page:
	  
	  > ![image](https://github.com/user-attachments/assets/8da20512-03f6-4770-9c48-b6f54d41f210)
	  
	  I'm not sure if a more recent update broke the fixes implemented in #29, or if this is the intended behavior, but it is really frustrating. Obviously I can just turn off the auto-parsing feature when creating new pages/adding page properties, but I don't always think about it, especially when I am in a hurry. I don't see any personal use cases where I would want to create automatic links in my properties. In the case that I wanted auto-links in my properties block, I could use the hotkey for auto-linking an individual block. Any help/suggestions??! 
	  
	  I really love this plugin and it has saved me a ton of time! However, the current functionality is driving me just a little crazy.
	  
	  Thanks in advance for any help!
- TODO [Title](URL)
  id:: 67039ad3-4ac2-44e8-91ce-16057e4f9c51
  collapsed:: true
	- Hello, I would like to know if it would be possible to identify the words contained in Aliases.  Like here for example.
	  
	  #+alias: word, here a phrase, wordb
	  
	  Thank you if you can add. Your complement is fantastic. It makes Logseq an exponentially more powerful tool. With resources like this, it would be unbeatable.
- TODO [Title](URL)
  id:: 67039ad3-63ae-4dc0-b48d-2714a0521256
  collapsed:: true
	- The PR handles 2 additional edge cases for code block and inline code detection.
	  
	  It also resolves an **Inefficient regular expression** code scan alert (see screenshot below) detected by [enabling Code Scanning](https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning#configuring-default-setup-for-a-repository) in my clone of your repository.
	  
	  PS - thank you for all of your amazing contributions!
	  
	  ![image](https://github.com/sawhney17/logseq-automatic-linker/assets/66134/eee81436-1454-4209-9f7d-8107ea37e26f)
- TODO [Title](URL)
  id:: 67039ad3-9f30-456f-972b-f46c00e498a0
  collapsed:: true
	- Hello
	  I am thankful for using this plugin
	  
	  When i choose template with retained formatting function and export page to pdf
	  The last part and the first part of the next page are cut off
	  
	  Could u solve this issue so that all the information comes out?
	  
	  Thanks
	  
	  <This is the example that i export>
	  ![스크린샷 2024-06-26 100032](https://github.com/sawhney17/logseq-pdf-export/assets/173860037/ef5b2fdc-2fd5-41c5-a569-88b1fb3395d7)
	  
	  
	  
	  <original content in logseq>
	  ![스크린샷 2024-06-26 100718](https://github.com/sawhney17/logseq-pdf-export/assets/173860037/80b1c99c-98db-4444-ab17-2a599cf49cda)
- TODO [Title](URL)
  id:: 67039ad3-fcfc-4edf-863a-59cb19c5b13a
  collapsed:: true
	- When working on a page, I take print to review my work. To do that, I take a print with a considerable margin to write reviews on it. Sometimes, those margins are half the size of the page. But it is beneficial when doing a review. 
	  
	  ## question
	  How can I get Margnie to use CSS or any other way to use this tool?
- TODO [Title](URL)
  id:: 67039ad3-2ca7-4d08-964c-d2fc771b0afb
  collapsed:: true
	- Added simple path settings for assets and pages to easily extract zip to hugo site. Perhaps simply adding content in front of pages would be better than having a setting for that.
- TODO [Title](URL)
  id:: 67039ad3-faa2-4602-8eb2-a373d35632c5
  collapsed:: true
	- 1. I want to create new nodes and relations.
	  2. Please give us some teaching videos.
- TODO [Title](URL)
  id:: 67039ad4-13c1-44b2-bc76-3b3834daf8ae
  collapsed:: true
	- Add Logseq title hierarchy to tags. Also add option to get page title with leaf title (last part of title hierarchy in Logseq).
	  
	  I've also simplified the tag push part.
- TODO [Title](URL)
  id:: 67039ad4-462e-4ca5-b155-cb9dfab5ae92
  collapsed:: true
	- null
- TODO [Title](URL)
  id:: 67039ad4-3b03-48c8-b978-535bcf669cee
  collapsed:: true
	- A simple archetype setting to add to frontmatter for each file.
- TODO [Title](URL)
  id:: 67039ad4-c716-4fce-9f99-b571ec4c58e8
  collapsed:: true
	- as the title says. some way of batch processing all pages and all blocks. I just started using this plugin, but I wouldn't like to have to go through every block and let it parse
- TODO [Title](URL)
  id:: 67039ad4-8600-42a6-8198-5fc6d4f969b9
  collapsed:: true
	- I wouldn't want to use automatic linking because it'll generate too many references, but it'd be good to simply highlight potential matches. This would already be a great starting point, but for bonus points it'd be great to have a `Link` prompt of some sort near the highlighted word, which would convert the highlight into an actual link.
	  
	  Similar to how [link-unlink](https://github.com/usoonees/logseq-plugin-link-unlink) plugin does it 
	  ![image](https://github.com/sawhney17/logseq-automatic-linker/assets/6875790/19cee323-2f25-4a10-9f65-df5cbe1b39ea)
- TODO [Title](URL)
  id:: 67039ad4-0e56-4097-863c-2d3d227fb6f7
  collapsed:: true
	- I have 3 different Calendly appointments on my schedule this week. Two are central time and one is showing as Pacific even though my calendar has it in Central time. The invite .ics shows Central time, and it is in Central time on my calendar, but it shows up at Pacific time in Logseq. Could it be using the sender's timezone?
- TODO [Title](URL)
  id:: 67039ad5-4843-43c8-b950-4d3cd7c8135d
  collapsed:: true
	- Are there any plans to support admonitions when exporting to PDF?
- TODO [Title](URL)
  id:: 67039ad5-ea80-478f-ac15-425f2bef1072
  collapsed:: true
	- Is there a way to use a smartblock button to invoke logseq-calendars-plugin?
- TODO [Title](URL)
  id:: 67039ad5-3b26-4bde-8af9-e7cb78b63fc0
  collapsed:: true
	- I've followed the README instructions for setting up Google iCal or Apple iCal integration unsuccessfully. Despite ensuring all steps and configurations were correctly implemented, the calendar fails to sync or connect, with “CALENDAR NOT FOUND” message.
	  
	  I'm seeking advice to diagnose and resolve this problem to get the Google iCal integration working properly
- TODO [Title](URL)
  id:: 67039ad5-edd8-4527-82d3-094cbbd44f30
  collapsed:: true
	- When I use the placeholder variable {Date} several time into the template setting, it only gets replaced by the actual date once.
	  
	  For instance, when I set the template setting like this :
	  ```
	  An event : {Date} - {Start} / {Date} - {End}
	  ```
	  
	  For an event where
	  - `{Date} = 2024-03-26`
	  - `{Start} = 11:00`
	  - `{End} = 12:30`
	  
	  It gets replaced by : 
	  ```
	  An event 2024-03-26 - 11:00 / {Date} 12:30
	  ```
	  
	  
	  Right now I'm using this template to create tasks from imported plugins : 
	  ```
	  LATER An event \nSCHEDULED: <{Date} d {Start}>
	  ```
	  
	  But I would have like to use this one : 
	  ```
	  LATER An event \nDEADLINE: <{Date} d {End}>\nSCHEDULED: <{Date} d {Start}>
	  ```
- TODO [Title](URL)
  id:: 67039ad5-5f64-4dd6-959c-52a090a8e841
  collapsed:: true
	- I am using logseq on Window 11, and I encounter below issues:
	  - the shortcut "command + shift + L: is not work. alternatively, "ctrl+shift" is work. idk why
	  - the shortcut "Command+P" also not work.
	  - Default short cut conflicts with other. So I change it but it is not applied.
- TODO [Title](URL)
  id:: 67039ad6-775a-45ce-b229-fd872fd60262
  collapsed:: true
	- For example I have a note regarding future meeting and I want to add event from Google Calendar to it, how can I do it? It seems like now I can import events only scheduled for today, not for a specific date.
- TODO [Title](URL)
  id:: 67039ad6-5494-4a58-8ca3-6a1c34b4e862
  collapsed:: true
	- null
- TODO [Title](URL)
  id:: 67039ad6-ec70-455e-b703-e02610de4082
  collapsed:: true
	- Hi,
	  I'm in an environment that does not have direct access to the internet. Can this plugin be installed and work without internet access?
	  Thanks
- TODO [Title](URL)
  id:: 67039ad6-2a5c-452c-a31a-b6de9d589e59
  collapsed:: true
	- Marking a block from the journal (a previous day), pressing the keyboard shortcut - that takes me to 'today' but it doesn't copy the content... It just takes me to today, that's it
- TODO [Title](URL)
  id:: 67039ad6-f810-456c-b5e0-76b1cd73b2c8
  collapsed:: true
	- Hi,
	  
	  I frequently use renderer blocks, for example `{{renderer code_diagram,d2,kroki.diagram.theme=300&kroki.diagram.sketch=1&containerStyle=width: 400px}}`
	  Unfortunately, if Automatic Linker parses the block - it completely wipes out the block and replaces it (with, for example [[Mar 8th, 2024]])
	  
	  Are we able to prevent this type of behaviour?
	  
	  In my context, I am using [Diagrams as Code](https://github.com/npgrosser/logseq-diagrams-as-code/) to render diagram blocks. I only started using this again today and all of my diagram blocks are being converted into links to todays journal.
	  
	  Thanks
- TODO [Title](URL)
  id:: 67039ad7-bd0c-4c33-847f-7b233a0ab269
  collapsed:: true
	- It took me a minute to realize that this was not a bug, but rather a missing feature that I expected to exist. When I type out a block and don't anticipate writing another at the moment, I often end the block by hitting `esc` instead of `enter`. When I do this, the plugin does not do the auto-parsing, yet this is the behavior I was expecting.
	  
	  Not sure if this is only an issue for me, or if others are in the same boat as me, but I thought I'd just document it.