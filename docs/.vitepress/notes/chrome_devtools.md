---
name: chrome-devtools
description: Visual inspection, DOM manipulation, console debugging, network tracing, and automated web audits (Lighthouse) via Chrome DevTools MCP.
---
# Chrome DevTools Integration Specialist

This skill outlines strategies and command guides for conducting automated web audits, visual inspect captures, DOM manipulation, console traces, and network profiling using the Chrome DevTools MCP.

## Connecting and Page Management

Initialize and manage active browser tabs:
-   **Open New Tab**: Use `new_page` to launch a new browser instance and return a unique target ID.
-   **Navigate to URL**: Use `navigate_page(url)` to load a website.
-   **Resize Window**: Adapt viewport dimensions using `resize_page(width, height)` to test mobile/tablet responsive break-points.

## Visual Auditing & Inspecting

Capture the layout state visually:
-   **Take Screenshot**: Use `take_screenshot` to save a PNG mockup of the rendered viewport.
-   **Take Snapshot**: Export the active DOM tree and CSS attributes using `take_snapshot` to analyze structure.

## Interacting and Script Execution

Simulate user interactions on the page:
-   **DOM Interactions**: Trigger actions using `click(selector)`, `hover(selector)`, or `fill(selector, text)` to interact with form fields.
-   **Custom JS Evaluation**: Execute arbitrary scripts in the page scope using `evaluate_script(script_string)` to query variables or trigger actions.

## Console & Network Audits

Trace background performance and errors:
-   **Console Logs**: Capture runtime errors using `list_console_messages` or `get_console_message`.
-   **Network Tracing**: Audit network request/response latency and headers using `list_network_requests`.
-   **Lighthouse Auditing**: Run automated audits on performance, accessibility, SEO, and best practices using `lighthouse_audit`.
