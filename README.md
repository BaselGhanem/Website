Architect Studio v4.0 - IDE Edition
Architect Studio v4.0 is a fully client-side, browser-based mini IDE for analyzing, editing, previewing, and exporting HTML projects.
It is designed for rapid inspection of existing code, not for greenfield development.
Strong opinion: this is not a code playground.
It is a code architecture inspector with editing powers.

Core Purpose


Paste a full HTML file.


Automatically decompose it into logical sections.


Edit each part independently.


Preview results instantly.


Export a clean production-ready project.



Key Features


RTL-first layout optimized for Arabic projects.


Ace Editor with syntax highlighting and autocomplete.


Automatic project parsing (HTML, CSS, JS, external libraries).


Intelligent JavaScript function detection and grouping.


Live Preview with real console interception.


Auto-save using localStorage.


One-click ZIP export.



Project Structure Parsing
When you paste a full HTML document, the IDE extracts:


External Libraries


<link> and external resource tags.




Styles (CSS)


All <style> blocks merged logically.




Components (HTML)


Each direct body child treated as an editable component.




JavaScript Logic


Functions classified into:


Init


Event


Logic






Opinionated choice: grouping JS by intent improves readability more than file-based splitting.

Live Preview Engine


Uses iframe with sandboxing enabled.


Rebuilds document on every valid change.


Injects a console interceptor script.


Captured console types:


log


warn


error


All messages appear in the built-in console panel.

IDE Toolbar Actions


Undo editor changes.


Add Bootstrap via CDN.


Add Tailwind via CDN.


Paste from clipboard.


Export full project as ZIP.


Export output contains:


index.html


style.css


script.js


Clean separation is enforced automatically.

Local Persistence


Project state is saved automatically.


Stored inside localStorage.


Reloading the page restores your last project.


Hard truth: this makes it safer than many online editors.

Technologies Used


HTML5


CSS3


JavaScript (Vanilla)


Ace Editor


JSZip


FileSaver.js


Zero build tools.
Zero backend.
Zero dependencies on frameworks.

Security Model


Preview runs inside sandboxed iframe.


Script execution is isolated.


No server-side execution.


This is as safe as a browser-only IDE gets.

Intended Audience


Front-End Developers.


Architects reviewing legacy HTML.


Trainers explaining code structure.


Developers who value clarity over noise.



Limitations


Not a full compiler.


No multi-file import.


Regex-based JS parsing is intentionally lightweight.


Opinion: accuracy over cleverness was the correct tradeoff here.

License
Open for personal and educational use.
Commercial redistribution requires author approval.

If you want, Basel, I can also:


Rewrite this README to GitHub-style minimal.


Add architecture diagrams.


Add screenshots section.


Turn it into a product landing README.

