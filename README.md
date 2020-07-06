### Prayer Timers

These are some cron alternatives for waking a user/reminding him of Prayer 15 
minutes before the Azan.
The time is based on Asia/Karachi timezone. You can always edit the time by
editing the related timer files.

## Dependencies

[mpv](https://mpv.io)
[systemd](https://systemd.io)

## Installation

Copy required files in `~/.config/systemd/user/`:

```sh
git clone https://gitlab.com/Abdullah/prayer-timers.git
mkdir -p ~/.config/systemd/user/
mkdir -p ~/.local/share/misc/
cd prayer-timers
cp *.timer ~/.config/systemd/user/
cp *.service ~/.config/systemd/user/
cp Kursi.ogg ~/.local/share/misc/
systemctl --user daemon-reload

# You can now invoke this to activate all timers.

systemctl enable --now {fajr,zuhr,asr,maghrib,isha}.timer
```
