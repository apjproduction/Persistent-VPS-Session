# 🧰 VPS Persistent Session Setup with tmux

This guide shows you how to install and use `tmux` on a Linux VPS to ensure your remote sessions continue running even if your local PC shuts down or your internet disconnects.

---

## 📥 Step 1: Connect to Your VPS (Replace your-username and your-vps-ip with your actual SSH credentials)

```bash
ssh your-username@your-vps-ip
```


Step 2: Install tmux

```bash
sudo apt install tmux
tmux new -s mysession
```


For CentOS/RHEL

```bash
sudo yum install tmux
```


Step 3: Start a tmux Session
# mysession is just a name. You can call it anything you like.

```bash
tmux new -s mysession
```


Step 4: Detach from the tmux Session

Ctrl + B, then D


Step 5: Reconnect to a tmux Session Later after Shutdown of PC

```bash
tmux attach -t mysession
```


# If you forget the session name or have multiple sessions, list them with:

```bash
tmux ls
```


Optional: Kill a tmux Session

```bash
tmux kill-session -t mysession
```


# TO Run Multiple Tmux Session

You can have multiple tmux sessions, each doing different things.

Inside a tmux session, you can split windows with:

.  Vertical split: Ctrl + B, then %

.  Horizontal split: Ctrl + B, then "
