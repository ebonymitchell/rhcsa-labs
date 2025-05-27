# Lab 02: Manage Groups and Sudo Privileges

## 🧠 Objective
Assign users to groups and configure sudo privileges.

---

## 🔧 Steps

1. **Create a new group called `wheel-watchers`:**

   ```bash
   sudo groupadd wheel-watchers

2. **Add `marshamcfly` to the `wheel` and `wheel-watchers` groups:**

   ```bash
   sudo usermod -aG wheel marshamcfly
   sudo usermod -aG wheel-watchers marshamcfly

3. ** Verify group membership:**
   groups marshamcfly
   id marshamcfly

4. ** Test sudo access:**
   sudo whoami


---

## 📓 Notes

- Encountered issues logging in and using `sudo` as `marshamcfly`
- Resolved by:
  - Logging in as root
  - Verifying user shell and home directory
  - Resetting password with `passwd marshamcfly`
  - Adding `marshamcfly` to `wheel` and `wheel-watchers` groups

---

## ✅ Outcome

✅ `marshamcfly` is a member of `wheel` and `wheel-watchers`  
✅ Password reset and login verified  
✅ Sudo access confirmed using `sudo whoami → root`  
✅ User is now fully configured and operational


