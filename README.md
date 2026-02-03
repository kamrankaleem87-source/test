# Digital Cammitii App (APK) - Plan (Roman Urdu)

## App ka Goal
Yeh app **BC/Committee** aur **Saving** system ke liye hogi. Admin aur Member dono ke alag login aur dashboards hongay. Final output **APK** file hogi jo aap direct install karke use kar sakein.

---

## Recommended Tech Stack (APK ke liye best)
- **Frontend + Mobile:** Flutter (Android APK build)
- **Backend:** Firebase (Auth, Firestore, Storage, Cloud Functions)
- **Notifications:** Firebase Cloud Messaging (FCM)
- **Live + Chat:** Firebase + WebRTC (future phase)
- **Reports/Export:** Cloud Functions + PDF generation

> Flutter se aapko **single codebase** se Android APK mil jata hai, is liye yeh best choice hai.

---

## Roles
### Admin
- Full access
- BC create karega (amount, members, duration)
- Members add karega
- Manual / Live / Live Camera BC open karega
- Payments approve / reject karega
- Reports aur summaries download karega

### Member
- Limited access, alag theme
- BC details aur history dekhega
- Payment screenshot + amount upload karega
- Status (Pending/Approved/Rejected) dekhega

---

## Core Features (aapke plan ke mutabiq)
1. **Admin & Member Separate Login**
2. **BC Creation with Auto Calculation**
   - Example: 50k / 10 members = 5k each
3. **Admin Unique ID + Password Setup**
4. **Member Dashboard**
   - Total BC amount
   - Member list
   - BC winner history
   - Filter by date + download summary
5. **BC Open Modes**
   - Live Lucky Draw (all members join hone par start)
   - Manual Order (sequence admin set karega)
   - Live Camera Mode (video call)
6. **Payment Upload System**
   - Screenshot + amount
   - Pending → Approved/Rejected
7. **WhatsApp Reminder (Coming Soon)**
8. **Live Chat (Text/Voice/Image)**

---

## APK Delivery Plan (Phases)
### Phase 1 (MVP)
- Admin + Member login
- BC creation + member add
- Dashboard (basic data)
- Payment upload + approval flow

### Phase 2
- Live lucky draw
- Manual order
- Notifications

### Phase 3
- Live camera + WhatsApp reminders
- Advanced reports + export

---

## Detailed Flow (Roman Urdu)
### Admin Flow
1. Admin signup → unique ID generate hoti hai → password admin khud set karta hai.
2. BC create: total amount + total members + duration months input.
3. Auto calculation: har member ka monthly share auto show hota hai.
4. Members add: name + phone/email + initial status.
5. BC open modes:
   - Live Lucky Draw (sab members join hone par start)
   - Manual Order (sequence admin set karta hai)
   - Live Camera (video call option)
6. Payments panel: member screenshots review → approve/reject.
7. Reports: date filter + summary download.

### Member Flow
1. Member login (admin share karta hai ID/password).
2. Dashboard: BC details, member list, winner history.
3. Payment upload: screenshot + amount → pending status.
4. Approve hone par tick icon.
5. Live draw join karein aur winner announcement dekhein.

---

## Suggested Screens (UI)
### Admin Screens
- Login / Signup
- Dashboard (BC list + stats)
- Create BC
- Members Management
- Live Draw / Manual Order
- Payments Approval
- Reports & Export

### Member Screens
- Login
- Dashboard (BC info + history)
- Payment Upload
- Live Draw / Manual Schedule
- Notifications

---

## Basic Database Schema (High-level)
### Collections (Firebase)
- `users` (admin/member)
  - id, role, name, phone, passwordHash
- `committees`
  - id, adminId, totalAmount, totalMembers, durationMonths, monthlyShare, status
- `members`
  - id, committeeId, userId, joinDate, orderNumber, hasWon
- `payments`
  - id, memberId, committeeId, amount, screenshotUrl, status, createdAt
- `draws`
  - id, committeeId, drawDate, mode, winnerMemberId
- `notifications`
  - id, userId, type, message, scheduledAt, sentAt

---

## APK Ready Checklist
1. Flutter project setup
2. Firebase integration
3. Auth + role based routing
4. Admin dashboard + member dashboard
5. Payment upload + approvals
6. Live draw (phase 2)
7. Notifications (phase 2)
8. Build APK + release testing

---

## Next Step
Bas bata dein:
- Aapko **Flutter** hi chahiye ya koi aur tech?
- Pehle **MVP** banana hai ya seedha full app?
- Aap apna **app name/logo** de sakte hain?

Phir main **UI flow + database schema + task breakdown** ko final shape me de dunga.
