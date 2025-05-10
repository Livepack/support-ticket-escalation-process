# Microsoft 365 Case Example: Exchange Online Mail Delivery Issue

## Problem Description (L1)

* **Impact**: User is unable to send emails externally; outbound messages remain in Outbox.
* **Environment**: Microsoft 365 Exchange Online, Outlook client version 2302, mail flow rule policies enabled.
* **Observed Behavior**: Emails to external domains are not leaving the user's mailbox.
* **Expected Behavior**: Messages should be delivered to external recipients without delay.

## Troubleshooting Steps Taken (L1 & L2)

* Verified user's Outlook is connected and syncing.
* Checked for known incidents on the Microsoft 365 Service Health Dashboard.
* Sent test messages internally and confirmed they were delivered successfully.
* Reviewed mail flow rules (transport rules) in the Exchange Admin Center.
* Confirmed user is not on a blocklist or quota limit.
* Used Message Trace: test external message stuck in "Pending" state.

## Finalize and Escalate (L2)

* **Issue Summary**: Outbound mail to external recipients remains in Outbox; internal mail works. No service-wide issues reported.
* **Troubleshooting Summary**:

  * Outlook connectivity and sync: ✅
  * Internal mail delivery: ✅
  * External mail delivery: ❌
  * Message trace: Status stuck in "Pending"
  * Policies reviewed: No blocking rules identified
* **Desired Result**: Ensure user is able to send mail externally as expected.

---

This example can be placed in the `examples/` folder of the repository to help support agents model their escalation descriptions effectively.
