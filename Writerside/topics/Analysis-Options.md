# Analysis Options

## Source code analysis options

(TBD)

## Web vulnerability analysis options


#### Login History File

A login history file is an .ecl format file saved from the Sparrow DAST event clipboard that records a user's behaviour at a specific URL. It is typically used when collecting or analysing URLs by storing the ID and password information that a user used to log in at a specific URL.
**If you attach a login history file** during URL collection and analysis, when you reach the URL where the Event Clipboard's recording started, it will reproduce the user's actions stored in the file. In this way, you can **pass the required authentication on the login page**. For more information about the Event Clipboard, see [Analysing with the Event Clipboard] (#Event-Clipboard-Analysis).


#### Using SSL certificates

Use SSL certificate means whether the URLs to be analysed are collected using the SSL certificate entered in the server settings if you need to set up an SSL certificate to access the internal site (default: `Yes`, `No`).
Setting this option to `Yes' will **use the SSL certificate entered in the server settings**, so HTTP clients will be able to access the web server only if they have that certificate. However, they will not be able to access web servers that require a certificate other than the SSL certificate you entered. If this option is set to `No', the web server will be accessed regardless of whether the SSL certificate required by the web server is trusted or not. Therefore, it is possible to access web servers that require an SSL certificate even if the SSL certificate is invalid or not entered in the server settings.


#### Client language

Sets what language the browser in which the web application being analysed is displayed is set to, and what language the HTTP client can understand. This can be entered in locale format, represented as **language_region** (default: `en_GB`)


#### Collection URLs to exclude

Gather URLs to exclude refers to a list of strings that, if the URL contains certain words, will be skipped without collecting the URL. You can enter one or more strings and separate them with an enter or comma (,).
If any of the words in the list you enter for this option are included in the URL you want to collect, then the URL will not be collected. However, the URL will be skipped just before it is collected so that the browser can still visit it.


#### Analytics URLs to exclude

Analyse URLs to exclude is a list of strings that skip the URL without analysing it if it contains certain words. You can enter one or more URLs and separate them with Enter or a comma (,).
If any of the words in the list you enter for this option are included in the URL you want to analyse, the URL will not be analysed.

> **Tip:** If you want to exclude the behaviour of a page, rather than the entire page represented by a URL, from analysis, use the **Exclude elements from performing events** option below.


#### URL suffixes to exclude

URL suffixes to exclude is a **list of suffixes that skip the end of a URL without collecting it if it contains certain words or extensions. You can enter them in the form of extensions starting with a period (.) and separated by an enter or comma (,). (Default: `.js, .css, .xml, .jpg, .jpeg, .gif, .bmp, .png, .ico, .wma, .wav, .mp3, .wmv, .avi, .mp4, .mov, .exe, .zip, .tar, . tar.gz, .7z, .doc, .xls, .ppt, .docx, .xlsx, .pptx, .pdf, .txt, .csv, .jar, .eot, .woff2, .woff, .ttf, .otf, .apk, .hwp`)
If any of the words in the **list** entered in this option are included at the end of the URL you want to collect, you will not collect that URL. We'll look at the attribute values of the HTML element, etc. before going to the URL and skip it, so you can skip it before downloading the file, etc.


#### Additional collection scope

If there are URLs you want to collect in addition to the ones you entered when adding or setting up your project, you can collect them here. However, the **additional collection scope** must be reachable from the URLs you set in the project or from URLs within the collection scope. You can enter one or more values as a string and separate them with an enter or comma (,).
Additional collection scope refers to URLs that are reachable from the URL being analysed but are not in the primary collection scope. Here, the primary collection scope of an analysis means URLs that are reachable from the analytics target URL entered in the project and have the same schema, such as http, and the same domain name or IP and port. For example, if your analytics target URL is `http://sparrow.com/main`, then even if you encounter a URL called `https://google.com` during ingestion, the rule of thumb is not to ingest it because it has a different schema or domain name. However, if you enter `google.com` in this option, you will collect `https://google.com`. You can enter more than one value and separate them with enter or a comma (,).
If the **list** you enter in this option contains any of the URLs in the list, they will be collected.


#### Event firing exclusion factors (CSS selector)

If the page contains any of the CSS selectors in the list entered in this option, the event will be fired for both the HTML element and its child HTML elements. You can enter one or more CSS selectors to exclude and separate them with an Enter or comma (,).
If the page contains any of the CSS selectors in the **list** entered in this option, the page will not fire all events on the corresponding HTML elements and child HTML elements. This is how you can **disable the logout button from being clicked** on a page.


#### Event Firing Additional Elements (CSS Selectors)

If the page contains at least one CSS selector from the list you enter in this option, it will fire the events of both the HTML element and its child HTML elements. You can enter one or more CSS selectors to add and separate them with an Enter or comma (,).
If the page contains any of the CSS selectors in the **list** entered in this option, it will fire the events of both the HTML element and its child HTML elements. In this way, you can **fire elements on your page that are not included in the event, such as tags.


#### Exclude elements from firing events (XPath)

If the page contains any of the XPaths in the list entered in this option, it will not fire all events for that HTML element and its child HTML elements. In this way, you can prevent users from clicking the Logout button on a page. You can enter one or more XPaths to exclude and separate them with an Enter or comma (,).
If the page contains any of the XPaths in the **list** entered in this option, the page will not fire any events on that HTML element and its child HTML elements. This is how you can **disable** clicking the logout button on a page.


#### Event Firing Additional Elements (XPath)

If the page contains at least one XPath from the list you enter in this option, it will fire the events of both the HTML element and its child HTML elements. You can enter one or more XPaths to add and separate them with an Enter or comma (,).
If any of the XPaths in the **list** you enter in this option are included on the page, they will fire the events of both the HTML element and its child HTML elements. In this way, you can **fire elements on your page that are not included in the event, such as tags.


#### Custom HTTP headers

Custom HTTP headers refers to a list of names and values for headers to be included in the HTTP request to be sent when collecting URLs. Entering the name and value of a header in this option will add that header to all HTTP request messages. You can add one or more headers by clicking the **Add** button and delete them by clicking the trash can icon.
This option requires you to **Enter headers that are required in HTTP requests**, which may slow down collection as it sets up a proxy in the browser.
With the exception of the `Cookie` header, **if you enter multiple headers with the same name, only one of them will be applied**. So if you need to enter multiple values, separate the header values with `;`. If a header with the same name already exists, it will be removed and a custom header will be added. To use custom headers, the host of the URL to be analysed must not be set to `localhost` or `127.0.0.1`. If you want to analyse a locally located web application, you must enter the local IP address.

