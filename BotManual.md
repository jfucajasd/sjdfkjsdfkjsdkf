# Bot Commands

---

## /genkey
**Description:** Generate a new admin key and DM it to a user.
**Usage:** `/genkey @user`
**Notes:**
- Each user can only hold one active key at a time
- If they already have one, revoke it first with `/revokekey`
- If the bot can't DM them, the key is shown to you instead

---

## /revokekey
**Description:** Deactivate a user's active key.
**Usage:** `/revokekey @user`
**Notes:**
- Takes effect on the Discord side instantly
- To enforce in-game, add the key to `REVOKED_KEYS` in the Lua script and re-inject

---

## /checkkey
**Description:** View active keys — all users or a specific one.
**Usage:**
- `/checkkey` — shows every active key
- `/checkkey @user` — shows only that user's key
**Shows:** Full key, use count, date generated, who generated it

---

## /listkeys
**Description:** Quick summary of all active keys.
**Usage:** `/listkeys`
**Shows:** Shortened key, username, use count

---

## /shutdown
**Description:** Shut the bot down cleanly.
**Usage:** `/shutdown`
**Notes:**
- Restart by SSHing into the server and running `python3 bot.py`
