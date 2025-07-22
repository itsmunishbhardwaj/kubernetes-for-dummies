# HAIC learnings

**Q. How to unpause a failed/stopped instance?**

**A.** `oc patch driverlessai 092f11be-d5f5-466b-9134-53f33fcd0c90.new-dai-engine-9751 -n aiem --type='merge' -p='{"spec":{"paused":false}}' `
