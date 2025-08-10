The script runs as a daemon (background process), which means:✅ You can close the terminal - the script keeps running
✅ Runs independently - doesn't need the terminal to stay alive
✅ Survives terminal closure - continues until you manually stop itHow it works:When you run python3 soundcloud_next.py start:Creates a background process (daemon)Stores the process ID in /tmp/auto_next_soundcloud.pidParent process exits (terminal can be closed)Child process continues running in backgroundTo manage it:# Start (then you can close terminal)
python3 soundcloud_next.py start

# Check if it's still running (from any terminal)
python3 soundcloud_next.py status

# Stop it (from any terminal)
python3 soundcloud_next.py stop

# Check logs (from any terminal)
cat /tmp/auto_next_soundcloud.logEven survives:✅ Closing terminal✅ Opening new terminal windows✅ Switching between apps✅ Computer sleep (will resume when awake)Only stops when:❌ You run the stop command❌ You restart your Mac❌ Chrome is completely quitSo yes, start it once and close the terminal - it will keep skipping songs every 2 minutes until you manually stop it! 🎵
