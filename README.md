# MetaDock MCP

Control the [MetaDock](https://metadock.app) desktop workspace over the **Model Context Protocol**.

MetaDock is a Windows power-user workspace that docks browsers and native apps side by side. Its
built-in MCP server exposes everything you can do by hand as tools, so Claude — or any MCP client —
can open and drive browsers, arrange layouts, manage bookmarks and downloads, search, and more.

Listed in the official MCP registry as **`app.metadock/metadock`**.

## What you can do

The server exposes **178 tools** across 11 groups — the full surface of what you can do in
MetaDock by hand:

| Group | Tools | Examples |
|---|---|---|
| **Browser** | 93 | navigate, execute JavaScript, click, type, screenshot, cookies, zoom, device emulation, fingerprint |
| **Layout & Profiles** | 25 | arrange/save/switch multi-browser layouts, per-profile proxy & settings |
| **Workspace** | 11 | manage and switch whole workspaces |
| **Native Apps** | 7 | mount/dismount and control docked native apps |
| **Ad-block** | 9 | toggle lists and per-site overrides |
| **Bookmarks** | 6 | read/write bookmarks and categories |
| **History** | 5 | query and manage browsing history |
| **Downloads** | 9 | start and manage downloads |
| **Search & Aliases** | 5 | search + custom aliases |
| **Permissions** | 4 | site permission control |
| **Settings** | 4 | app settings |

### Full tool list

<details>
<summary><b>Browser</b> (93 tools)</summary>


- `browser_batch` — Execute multiple browser operations in sequence on one or multiple browsers (100 operations per browser max)

- `browser_clear_cache` — Clear this browser's HTTP cache (CDP Network.clearBrowserCache)

- `browser_clear_console` — Clear console messages for the browser

- `browser_clear_cookies` — Clear all cookies for the browser

- `browser_clear_device_emulation` — Clear device emulation for the browser

- `browser_clear_fingerprint` — Disable all fingerprint spoofing for a browser

- `browser_clear_geolocation` — Clear geolocation override for the browser

- `browser_clear_input` — Clear an input field

- `browser_clear_storage` — Clear the page's localStorage or sessionStorage

- `browser_click` — Click an element by CSS selector

- `browser_click_at` — Click at raw viewport pixel coordinates using a real (trusted) mouse event

- `browser_close` — Close a browser instance

- `browser_close_devtools` — Close developer tools for the browser

- `browser_create` — Create a new browser instance

- `browser_delete_cookie` — Delete a specific cookie from the browser

- `browser_drag` — Drag from one element to another using real (trusted) mouse events: press at the source center, move in steps to the tar…

- `browser_emulate_device` — Enable device emulation for the browser

- `browser_enable_devtools` — Enable or disable developer tools for the browser

- `browser_execute_js` — Execute JavaScript code in browser

- `browser_extract` — Structured, schema-driven extraction

- `browser_find` — Find visible interactive elements whose role or accessible name matches a text query

- `browser_get_all_cookies` — Get all cookies for the browser

- `browser_get_console` — Get console messages from the browser

- `browser_get_cookie` — Get a cookie value from the browser

- `browser_get_element_attribute` — Get an attribute value of an element by CSS selector

- `browser_get_element_box` — Get an element's bounding box (x/y/width/height/top/left/bottom/right) and key computed styles (display, visibility, opa…

- `browser_get_element_text` — Get the text content of an element by CSS selector

- `browser_get_fingerprint` — Get current fingerprint spoofing configuration for a browser

- `browser_get_forms` — Enumerate forms and their fields {name, id, type, label, placeholder, required, options, selector}

- `browser_get_last_dialog` — Get the most recent JavaScript dialog captured for this browser (only captured while a non-default dialog policy is acti…

- `browser_get_links` — Extract all hyperlinks on the page as a compact list of {text, href, rel}

- `browser_get_metadata` — Get page metadata: title, description, canonical URL, author, published/modified dates, language, favicon, Open Graph + …

- `browser_get_network` — List the network requests the page has made (from the Resource Timing API): url, type, protocol, size, and duration, plu…

- `browser_get_screenshot` — Retrieve a saved screenshot by UUID

- `browser_get_source` — Get raw page source HTML

- `browser_get_state` — Get comprehensive browser state

- `browser_get_storage` — Read the page's localStorage or sessionStorage

- `browser_get_tables` — Extract HTML tables as markdown (default), CSV, or JSON rows

- `browser_get_title` — Get current page title

- `browser_get_url` — Get current URL of a browser

- `browser_get_zoom` — Get current zoom factor for the browser

- `browser_go_back` — Navigate browser back in history

- `browser_go_forward` — Navigate browser forward in history

- `browser_history_go` — Move within the browser's session history by a relative delta (e.g

- `browser_hover` — Hover the pointer over an element (dispatches pointer/mouse enter+over+move events), triggering hover menus and tooltips

- `browser_inject_css` — Inject CSS into the page

- `browser_inject_script` — Inject a script URL into the page

- `browser_is_element_visible` — Check if an element is visible on the page

- `browser_navigate` — Navigate a browser to a specific URL

- `browser_open_devtools` — Open developer tools for the browser

- `browser_press_key` — Send a real (trusted) key press to the focused element via native input

- `browser_print_pdf` — Print page to PDF

- `browser_read` — Read the page as clean, LLM-friendly content instead of raw HTML

- `browser_reload` — Reload the current page

- `browser_remove_header` — Remove a previously-set custom request header from this browser

- `browser_right_click` — Right-click (context-menu) an element by dispatching mousedown/mouseup/contextmenu with the secondary button

- `browser_screenshot` — Take a screenshot of the page - returns base64-encoded PNG image data

- `browser_screenshot_element` — Screenshot a single element (scrolls it into view, captures just its bounding box)

- `browser_scroll_by` — Scroll by offset amount

- `browser_scroll_to` — Scroll to specific coordinates

- `browser_set_cookie` — Set a cookie for the browser

- `browser_set_dialog_policy` — Control how this browser handles JavaScript dialogs (alert/confirm/prompt/beforeunload)

- `browser_set_fingerprint` — Set fingerprint spoofing config for a browser

- `browser_set_fingerprint_audio` — Configure audio fingerprint spoofing for a browser

- `browser_set_fingerprint_canvas` — Configure canvas fingerprint spoofing for a browser

- `browser_set_fingerprint_webgl` — Configure WebGL fingerprint spoofing for a browser

- `browser_set_geolocation` — Set geolocation for the browser

- `browser_set_header` — Add or override a custom HTTP request header sent by this browser on subsequent requests (e.g

- `browser_set_headless` — Toggle headless mode for a browser

- `browser_set_muted` — Mute or unmute a single browser's audio

- `browser_set_offline` — Set offline mode for the browser

- `browser_set_storage` — Set a key in the page's localStorage or sessionStorage

- `browser_set_user_agent` — Set user agent for the browser

- `browser_set_value` — Set value of an input element

- `browser_set_viewport` — Set viewport size for the browser

- `browser_set_zoom` — Set zoom factor for the browser

- `browser_snapshot` — Token-efficient interactive snapshot: a compact list of visible interactive elements (links, buttons, inputs, selects) e…

- `browser_stop` — Stop loading the current page

- `browser_submit_form` — Submit a form

- `browser_type` — Type text at current cursor position

- `browser_upload_file` — Attach files to a file <input> element

- `browser_wait_for_element` — Wait for an element to appear on the page

- `browser_wait_for_load` — Wait for page to finish loading

- `browser_wait_for_network_idle` — Wait until the page has finished loading and no new network requests have started for a quiet period

- `browsers_close_all` — Close all browsers

- `browsers_close_others` — Close all browsers except one

- `browsers_close_others_in_layout` — Close all browsers in a layout except one

- `browsers_create_multiple` — Create multiple browsers with different configurations

- `browsers_execute_all` — Execute JavaScript on all browsers and return each browser's result

- `browsers_get_urls` — Get every open browser's uuid, url and title (copy all URLs)

- `browsers_list` — List all browsers

- `browsers_navigate_all` — Navigate all browsers to a URL

- `browsers_reload_all` — Reload all browsers


</details>

<details>
<summary><b>Layout & Profiles</b> (25 tools)</summary>


- `layout_close_all` — Close all dock widgets of specified types

- `layout_create` — Create a new layout/dock

- `layout_delete` — Delete a layout/dock

- `layout_equalize` — Equalize the dock splitters so the tiled docks share space evenly (tidy up the layout)

- `layout_get_apps` — Get applications in a layout

- `layout_get_browsers` — Get browsers in a layout

- `layout_get_info` — Get information about a layout

- `layout_list` — List all available layouts/docks

- `layout_open_dock` — Open a non-browser dock in the layout: a downloads panel, history panel, or new-window panel

- `layout_rename` — Rename a layout/dock

- `layout_reset_resolution` — Clear a custom layout resolution and return the window to free/auto sizing

- `layout_screenshot` — Take a screenshot of the entire layout window at its exact dimensions

- `layout_set_locked` — Lock or unlock a layout

- `layout_set_mute_all` — Mute or unmute all browsers in the layout at once

- `layout_set_resolution` — Set a fixed pixel resolution for the layout window (useful for consistent screenshots or device-size testing)

- `layout_toggle_fullscreen` — Toggle fullscreen mode for the layout window

- `profile_create` — Create a new browser profile

- `profile_create_temporary` — Create a temporary browser profile

- `profile_delete` — Delete a browser profile

- `profile_get_default` — Get default browser profile

- `profile_get_proxy` — Get the proxy address stored for a browser profile

- `profile_list` — List all browser profiles

- `profile_rename` — Rename a browser profile (automatically handles both regular and temporary profiles)

- `profile_set_default` — Set default browser profile

- `profile_set_proxy` — Set the proxy address for a browser profile


</details>

<details>
<summary><b>Workspace</b> (11 tools)</summary>


- `workspace_create` — Create a new workspace

- `workspace_delete` — Delete a workspace

- `workspace_get_current` — Get the currently active workspace

- `workspace_get_info` — Get information about a workspace

- `workspace_get_layouts` — Get all layouts associated with a workspace

- `workspace_get_startup` — Get the startup workspace information

- `workspace_list` — List all available workspaces

- `workspace_rename` — Rename a workspace

- `workspace_set_homepage` — Set workspace homepage URL

- `workspace_set_startup` — Set workspace as startup workspace

- `workspace_switch` — Switch to a different workspace


</details>

<details>
<summary><b>Native Apps</b> (7 tools)</summary>


- `app_dismount` — Dismount (unembed) a native app dock by UUID

- `app_info` — Get full info for a mounted native app by UUID

- `app_list` — List native app docks mounted in a layout (full JSON)

- `app_list_processes` — List running OS windows/processes that can be mounted as native app docks

- `app_lock` — Lock or unlock a native app dock

- `app_mount` — Mount a running native window as a dock in a layout

- `app_set_title` — Set the custom title of a native app dock


</details>

<details>
<summary><b>Ad-block</b> (9 tools)</summary>


- `adblock_add` — Add a new adblock filter list by URL

- `adblock_enable` — Enable or disable an adblock filter list by id

- `adblock_get_override` — Get a profile's adblock override (on/off/inherit) and the effective enabled state

- `adblock_list` — List all adblock filter lists (id, name, url, enabled, rule_count, last_updated)

- `adblock_remove` — Remove an adblock filter list by id

- `adblock_set_auto_update` — Configure periodic auto-update of filter lists

- `adblock_set_override` — Set a profile's adblock override

- `adblock_update` — Trigger a refresh/download of a single filter list by id

- `adblock_update_all` — Trigger a refresh/download of all enabled filter lists


</details>

<details>
<summary><b>Bookmarks</b> (6 tools)</summary>


- `bookmark_create` — Create a bookmark

- `bookmark_delete` — Delete a bookmark by id

- `bookmark_list` — List bookmarks (id, name, url, category_id, tags)

- `bookmark_list_categories` — List bookmark categories (id, name, parent_id, color, path, depth)

- `bookmark_open` — Open a bookmark in a new browser

- `bookmark_update` — Update a bookmark's title, url, and/or category by id (unspecified fields keep their current value)


</details>

<details>
<summary><b>History</b> (5 tools)</summary>


- `history_clear` — Clear all browsing history across every profile

- `history_delete_visit` — Delete a single history visit by visit_id

- `history_list` — List/search browsing history visits (visit_id, uri, title, host, profile, visit_time, counts)

- `history_profiles` — List distinct profiles that have history visits

- `history_remove_uri` — Remove all history for a specific URL


</details>

<details>
<summary><b>Downloads</b> (9 tools)</summary>


- `download_cancel` — Cancel an in-flight download

- `download_clear_all` — Remove every download (cancels in-flight first)

- `download_clear_completed` — Remove all completed/cancelled/failed downloads

- `download_get` — Get one download by uuid

- `download_list` — List active/recent downloads (uuid, filename, url, status, bytes, speed)

- `download_pause` — Pause an in-flight download

- `download_remove` — Remove a download from the list (cancels first if active)

- `download_resume` — Resume a paused download

- `download_start` — Download a URL directly to the app's configured download directory


</details>

<details>
<summary><b>Search & Aliases</b> (5 tools)</summary>


- `alias_delete` — Delete a website alias

- `alias_list` — List website aliases (short keyword -> URL shortcuts used in the omnibox)

- `alias_resolve` — Resolve a website alias to its URL

- `alias_set` — Create or update a website alias

- `search` — Run a search query in a new browser using the default (or specified) search engine


</details>

<details>
<summary><b>Permissions</b> (4 tools)</summary>


- `permission_clear` — Forget every remembered permission decision for all hosts

- `permission_list` — List all remembered site permission decisions (host, permission_type, label, allowed)

- `permission_remove` — Forget one remembered permission decision for a host

- `permission_remove_host` — Forget every remembered permission decision for a host


</details>

<details>
<summary><b>Settings</b> (4 tools)</summary>


- `settings_get` — Get current values of application settings (the readable counterpart to settings_set) - behaviour/features, appearance, …

- `settings_list_search_engines` — List configured search engines (id, name, url)

- `settings_list_themes` — List available themes (id, name, is_dark, is_core)

- `settings_set` — Set an application setting by key


</details>


## Requirements

- The **MetaDock desktop app** installed and running (Windows). Get it at **[metadock.app](https://metadock.app)**.
- The MCP server enabled in **MetaDock → Settings → API & Automation**.

The server runs **locally** on your machine — stdio (`metadock mcp`) or loopback HTTP — so your data
never leaves your computer.

## Install

### Option A — from inside MetaDock (recommended)

**Settings → API & Automation → Install to desktop tools**, then pick your client (Claude Desktop,
Claude Code, Cursor, VS Code, Codex, …). MetaDock writes the correct config and enables the endpoint
for you.

### Option B — Claude Desktop (.mcpb)

Download the latest `metadock-<version>.mcpb` from [Releases](../../releases), open it with Claude
Desktop, and confirm the path to `metadock.exe` when prompted.

### Option C — manual (any stdio MCP client)

Add this to your client's MCP config, adjusting the path to where MetaDock is installed
(default `%LOCALAPPDATA%\MetaDock\bin\metadock.exe`):

```json
{
  "mcpServers": {
    "metadock": {
      "command": "C:\\Users\\YOU\\AppData\\Local\\MetaDock\\bin\\metadock.exe",
      "args": ["mcp"]
    }
  }
}
```

### Option D — official MCP registry

Any registry-aware client can discover the server by name: **`app.metadock/metadock`**.

## Privacy & safety

Everything runs on your machine. By design, the following are **not** reachable over MCP (or any
automation surface): the Password Vault, the AI assistant, profile-bundle import/export, and the
system clipboard.

## Links

- Website — https://metadock.app
- MCP setup docs — https://metadock.app/docs/mcp
- Support — https://metadock.app/support
- Privacy policy — https://metadock.app/privacy

## Notes

- The `.mcpb` in Releases is currently **unsigned**; Claude Desktop will note this on install.
- This bundle references your installed `metadock.exe` and launches `metadock mcp` — the app itself
  is not bundled.
