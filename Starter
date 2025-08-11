mkdir -p ~/bin
cat > ~/bin/SoundCloud <<'EOF'
#!/bin/zsh
case "$1" in
  start|Start|START)
    python3 /Users/nickinoz/myMindPalace/MusicSkipper/soundcloud_next.py start
    ;;
  stop|Stop|STOP)
    python3 /Users/nickinoz/myMindPalace/MusicSkipper/soundcloud_next.py stop
    ;;
  *)
    echo "Usage: SoundCloud start|stop"
    exit 1
    ;;
esac
EOF
chmod +x ~/bin/SoundCloud
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc   # add only once
source ~/.zshrc
