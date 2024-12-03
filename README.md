# strapi-plugin-audit-trail

A comprehensive audit trail plugin for Strapi that tracks user activities.

This plugin utilizes a middleware to create an audit log of user activities. The audit log is accessible in the Audit Trail content type. The admin page provides a functionality to clear audit trails.

**This is a customized version of [strapi-plugin-audit-trail](https://github.com/10Life/strapi-plugin-audit-trail), originally developed by Roy To.**

## Changes in this version

- Hidden the Strapi control panel for specific use cases.
- Added maintainers for this forked version.

Maintained by: [b159732000](https://github.com/b159732000).

## How to use

To enable this plugin, put the following code in `/config/plugin.js`:

```javascript
  'audit-trail': {
    enabled: true,
  },
```

Add in /config/middleware.js

```javascript
module.exports = ({ env }) => [
  \\ other middleware
  'plugin::audit-trail.logActivity'
];
```

## Road Map

- provide config for audit items
