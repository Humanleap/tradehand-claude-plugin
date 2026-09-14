# Tradehand for Claude

Browse UK tradespeople by trade and location, view profiles and services, and prepare an instant quote or booking review. Confirm the booking and any payment on Tradehand.

## What you can do

- Search local tradespeople by trade and place
- Open a profile and its services
- Prepare an instant quote or a booking to review
- Continue on Tradehand to confirm and pay

Bookings and payments are confirmed only on Tradehand. Claude does not take payment, hold deposits, issue refunds, or guarantee a price or slot.

## Install

### Connector

In Claude, add a custom connector:

- MCP endpoint: `https://tradehand.com/api/mcp` (Streamable HTTP)
- Auth callback: `https://claude.ai/api/mcp/auth_callback`

Sign in when Claude asks, then ask it to find a tradesperson near you.

### Plugin

This directory is the public Claude plugin package (`tradehand` 0.1.0). Install it, then use the MCP endpoint above.

## Package

- Homepage: [tradehand.com/developers](https://tradehand.com/developers)
- Repository: [github.com/Humanleap/tradehand-claude-plugin](https://github.com/Humanleap/tradehand-claude-plugin)
- License: MIT
- Author: Outside HQ LTD
