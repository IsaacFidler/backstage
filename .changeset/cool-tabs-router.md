---
'@backstage/ui': patch
---

Fixed client-side navigation for container components by wrapping the container (not individual items) in RouterProvider. Components now conditionally provide routing context only when children have internal hrefs, removing the Router context requirement when not needed. This also removes the need to wrap these components in MemoryRouter during tests when they are not using the href prop.

Affected components: Tabs, Tab, TagGroup, Tag, Menu, MenuItem, MenuAutocomplete
