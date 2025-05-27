# Lab 03: Create a Sudo User – `mcfly`

## 🧠 Objective  
Create a new user with sudo privileges and verify elevated access.

---

## 🔧 Steps

1. **Create a new user called `mcfly`:**

   ```bash
   sudo useradd -m mcfly
   ```

2. **Set a password for `mcfly`:**

   ```bash
   sudo passwd mcfly
   ```

3. **Add `mcfly` to the `wheel` group for sudo access:**

   ```bash
   sudo usermod -aG wheel mcfly
   ```

4. **Verify group membership:**

   ```bash
   id mcfly
   ```

5. **Switch to the new user:**

   ```bash
   su - mcfly
   ```

6. **Test sudo access:**

   ```bash
   sudo whoami
   ```

---

## 📝 Notes

- Initially ran into password errors:
  - Password too short
  - Password mismatch
  - Dictionary check failed
- Successfully set password after 3 attempts.
- Used `usermod` to add `mcfly` to the `wheel` group.
- Verified group membership with `id`.
- Verified sudo access with `sudo whoami`.

---

## ✅ Outcome  
New user `mcfly` was successfully created with sudo privileges.  
Sudo access confirmed — `whoami` returned `root`.
