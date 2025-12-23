Files in this directory contain overrides that will be appended
before </body> using a script like this:

    sed -i '.bak' '/<\/body>/r firelight-overrides/${{ matrix.document.url }}.html' dist/${{ matrix.document.url }}/index.html

Files must be named after document URL
(e.g., plateaudocument or plateaudocument02).
