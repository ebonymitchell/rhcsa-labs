# Lab 02: Manage Groups and Sudo Privileges

## 🧠 Objective
Assign users to groups and configure sudo privileges.

---

## 🛠️ Steps

1. **Create a new group called `wheel-watchers`:**

    ```bash
    sudo groupadd wheel-watchers
    ```

2. **Add `marshamcfly` to the `wheel` and `wheel-watchers` groups:**

    ```bash
    sudo usermod -aG wheel marshamcfly
    sudo usermod -aG wheel-watchers marshamcfly
    ```

3. **Verify group membership:**

    ```bash
    groups marshamcfly
    id marshamcfly
    ```

4. **Test sudo access:**

    ```bash
    sudo whoami
    ```

---

## 📓 Notes

- Had login issues with `marshamcfly` after group changes
- Resolved by:
  - Resetting password
  - Verifying group assignments
  - Logging out and back in to refresh group permissions

---

## ✅ Outcome

✅ `marshamcfly` is a member of `wheel` and `wheel-watchers`  
✅ Password reset and login verified  
✅ Sudo access confirmed using `sudo whoami` → `root`

