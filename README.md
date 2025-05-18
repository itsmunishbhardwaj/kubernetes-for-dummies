# kubernetes-for-dummies

## FAQ's

### Q. What is busy box?
Great question!

🧰 What is busybox?

busybox is a tiny Linux utility that bundles many common UNIX/Linux command-line tools into a single lightweight executable. Think of it as a Swiss Army knife for containers.

⸻

🧠 Why use it?
	•	✅ It includes commands like: sh, cp, mkdir, ls, cat, etc.
	•	✅ It’s super small (a few MB) — perfect for init containers.
	•	✅ It doesn’t need a full Linux OS image like ubuntu or alpine.

⸻

📦 In Kubernetes

In Kubernetes, busybox is often used in:
	•	initContainers to do pre-setup tasks (like copying files)
	•	debug containers where a full OS isn’t needed
	•	probes and simple exec jobs

⸻

🧪 Example

If you run:

kate run debug --image=busybox -it --restart=Never -- sh

You’ll drop into a minimal shell where you can run commands like:

mkdir /mydir
echo hello > /mydir/test.txt
cat /mydir/test.txt

All with just a few MB of image pull time.

⸻

So in your case, busybox is perfect for copying your Hadoop XML files into the right directory — no bloat, no extra dependencies.
