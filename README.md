---

# ✅ SaaS V1 – User Validation Checklist

## 🏢 Tenant / Company Onboarding

* [x] Company created successfully
* [x] Unique tenant ID generated
* [x] Default roles created (Admin, Member, Viewer)
* [x] Default department created
* [x] Tenant cannot access other tenants’ data
* [x] Tenant-scoped APIs enforced
* [x] Tenant-specific audit logs verified

---

## 🔐 Authentication & Login

* [x] Login succeeds with valid credentials
* [x] Login fails with invalid credentials
* [x] Session/token created correctly
* [x] Token expires as expected
* [x] Logout invalidates token
* [ ] Rate limiting on login attempts works *(later)*
* [ ] Multiple failed attempts handled safely *(later)*

---

## 👤 Users – Create / Update / Remove

### ➕ User Creation

* [x] Admin can create a user (invite without email)
* [ ] Invite email delivered *(later)*
* [ ] Invite link works only once *(later)*
* [ ] Invite expiry enforced *(later)*
* [ ] User sets password successfully
* [x] User linked to correct tenant

### 📝 User Update

* [x] User name can be updated
* [ ] User email update handled correctly
* [x] Role can be changed
* [x] Department assignment updated
* [x] Changes take effect immediately
* [x] Changes logged in audit log

### 🚫 User Deactivation / Deletion

* [ ] User can be deactivated *(later)*
* [ ] Deactivated user cannot log in *(later)*
* [ ] Active sessions revoked on deactivation *(later)*
* [ ] User can be deleted *(if supported — later)*
* [ ] Deleted user cannot access platform *(later)*
* [ ] No orphan data remains *(later)*

---

## 🔑 Roles & Permissions

* [x] Role created successfully
* [x] Role permissions updated correctly
* [x] Role assigned to user
* [x] Role change reflects immediately
* [x] Allowed actions succeed
* [x] Forbidden actions blocked (403)
* [ ] UI hides unauthorized actions
* [ ] Backend enforces permissions independently

---

## 🗂️ Departments / Teams

* [x] Department created
* [x] Department renamed
* [x] Department deleted safely
* [x] User assigned to department
* [x] User removed from department
* [x] Department scoping enforced
* [ ] Deleting department does not break users(not implementated in ui)

---

## 🧩 Core SaaS Features (repeat per feature)

* [ ] Feature visible only to permitted roles
* [x] Unauthorized access blocked at API
* [x] Create operation works
* [x] Read operation returns correct data
* [x] Update operation persists correctly
* [x] Delete operation handled safely
* [x] Tenant isolation enforced

---

## 📝 Audit Logs

* [x] Login/logout events logged
* [ ] User creation logged
* [ ] User updates logged
* [ ] Role changes logged
* [ ] Permission changes logged
* [ ] Sensitive actions logged
* [x] Logs are immutable
* [x] Logs are tenant-scoped
* [x] Logs show correct actor and timestamp

---

## 🔒 Security & SaaS Guardrails

* [x] Unauthorized API calls blocked
* [x] Cross-tenant access impossible
* [x] IDOR vulnerabilities tested
* [x] Tokens invalid after logout
* [x] Sensitive data not leaked in logs
* [x] Errors do not expose internals

---

## 🔁 Regression Scenarios

* [ ] Create tenant → add users → assign roles → use features
* [ ] Downgrade role → permissions revoked immediately
* [ ] Deactivate user → access blocked instantly
* [ ] Delete department → no orphan data
* [ ] Role deletion handled safely

---

## 🏁 Final Validation

* [ ] All critical SaaS flows verified
* [ ] No cross-tenant data leakage
* [ ] Permissions enforced consistently
* [ ] Audit logs reliable and complete
* [ ] Ready for pilot / production

---
