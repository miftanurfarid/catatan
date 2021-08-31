sudo cp /etc/systemd/system/snapper-boot.service /etc/systemd/system/snapper-boot-home.service
sudo cp /etc/systemd/system/snapper-boot.timer /etc/systemd/system/snapper-boot-home.timer
sudo sed -i 's/config root/config home/' /etc/systemd/system/snapper-boot-home.service


sudo cp /etc/systemd/system/snapper-boot.service /etc/systemd/system/snapper-boot-var.service
sudo cp /etc/systemd/system/snapper-boot.timer /etc/systemd/system/snapper-boot-var.timer
sudo sed -i 's/config root/config var/' /etc/systemd/system/snapper-boot-var.service


sudo cp /etc/systemd/system/snapper-boot.service /etc/systemd/system/snapper-boot-local.service
sudo cp /etc/systemd/system/snapper-boot.timer /etc/systemd/system/snapper-boot-local.timer
sudo sed -i 's/config root/config local/' /etc/systemd/system/snapper-boot-local.service


sudo cp /etc/systemd/system/snapper-boot.service /etc/systemd/system/snapper-boot-srv.service
sudo cp /etc/systemd/system/snapper-boot.timer /etc/systemd/system/snapper-boot-srv.timer
sudo sed -i 's/config root/config srv/' /etc/systemd/system/snapper-boot-srv.service


sudo cp /etc/systemd/system/snapper-boot.service /etc/systemd/system/snapper-boot-su.service
sudo cp /etc/systemd/system/snapper-boot.timer /etc/systemd/system/snapper-boot-su.timer
sudo sed -i 's/config root/config su/' /etc/systemd/system/snapper-boot-su.service


sudo cp /etc/systemd/system/snapper-boot.service /etc/systemd/system/snapper-boot-opt.service
sudo cp /etc/systemd/system/snapper-boot.timer /etc/systemd/system/snapper-boot-opt.timer
sudo sed -i 's/config root/config opt/' /etc/systemd/system/snapper-boot-opt.service


sudo snapper -c root set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0

sudo snapper -c home set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0

sudo snapper -c var set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0

sudo snapper -c local set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0

sudo snapper -c srv set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0

sudo snapper -c su set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0

sudo snapper -c opt set-config TIMELINE_LIMIT_DAILY=3-10 TIMELINE_LIMIT_HOURLY=4-10 TIMELINE_LIMIT_MONTHLY=0 TIMELINE_LIMIT_WEEKLY=2-10 TIMELINE_LIMIT_YEARLY=0