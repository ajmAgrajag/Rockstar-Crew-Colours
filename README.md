# Rockstar Crew Colors Bookmarklet

This project provides a simple way to set custom crew colors on Rockstar Social Club using a bookmarklet. By leveraging JavaScript, users can apply non-standard HEX codes as crew colors, including those not natively supported by the Social Club interface.

---

## Features

- Allows for non-standard HEX codes to be applied as crew colors.
- Automatically appends valid suffixes to non-working HEX codes until a supported combination is found.

---

## Disclaimer

This tool is an independent creation and is **not affiliated with, endorsed by, or approved by Rockstar Games, Take-Two Interactive, or any of their subsidiaries**. It is provided for educational and personal use only.

**Users are responsible for ensuring that their use of this tool complies with Rockstar's Terms of Service.** Rockstar may prohibit or restrict the use of third-party tools that modify or interact with its services in unintended ways, and it is the user's responsibility to avoid any actions that may violate those terms.

By using this tool, you agree to:
- Only use it for personal, non-commercial purposes.
- Avoid any usage that could be considered exploitative, malicious, or harmful to Rockstar's services or community.

The author(s) of this tool are not liable for any actions taken against your account as a result of using this tool. If you're unsure whether this tool complies with Rockstar's policies, please refer to [Rockstar's Terms of Service](https://www.rockstargames.com/legal).

---

## How to Use

### 1. Add the Bookmarklet to Your Browser
To use the tool, you need to add the bookmarklet to your browser's bookmarks:

1. Copy the following code:

    ```javascript
    javascript:(function(){const script=document.createElement('script');script.src='https://ajmagrajag.github.io/Rockstar-Crew-Colours/colourTool.js';document.body.appendChild(script);})();
    ```

2. Open your browser's bookmarks bar.
3. Right-click on the bar and choose **"Add Page"** or **"Bookmark this page"**.
4. Enter a name for the bookmark (e.g., `Rockstar Crew Colors`) and paste the code into the **URL** field.
5. Save the bookmark.

---

### 2. Run the Bookmarklet on Rockstar Social Club
1. Go to the **Manage Crew** section of Rockstar Social Club:
   - Example URL: `https://socialclub.rockstargames.com/crew/YOUR_CREW_NAME/manage/edit`
2. Click on the bookmarklet you just saved.
3. When prompted, enter your desired HEX color code (e.g., `#262425` or `262425ff`).
4. The tool will:
   - Validate your HEX code.
   - Attempt to set the color directly if it's supported.
   - If not supported, it will append suffixes like `ff`, `a`, etc., to find a working combination.

5. A success or failure message will appear.

---

## Troubleshooting

### The Prompt Doesn't Appear
If the prompt doesn't appear after clicking the bookmarklet:
- Ensure you are on the **Manage Crew** page of Rockstar Social Club.
- Check your browser's developer console for errors (`F12` → **Console** tab).
- Make sure the script URL in your bookmarklet is correct.
- Try refreshing the page

### The HEX Code Doesn't Work
If your HEX code doesn't work:
- Ensure the HEX code is 6 or 8 characters long (e.g., `262425` or `262425ff`).
- The tool will automatically append valid suffixes, but not all colors are supported by Rockstar.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

### Acknowledgments

- Credit to Furry_Monkey who came up with the original bookmarklet. This is a feature-lite version
- **Rockstar Games** is a trademark of **Take-Two Interactive**, and all related marks and services are their property.
