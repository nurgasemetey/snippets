### thread mmap count


[Tuning MongoDB &amp; Linux to allow for tens of thousands connections | MongoDB](https://www.mongodb.com/blog/post/tuning-mongodb--linux-to-allow-for-tens-of-thousands-connections "Tuning MongoDB &amp; Linux to allow for tens of thousands connections | MongoDB")


 

```
echo 9999999 > /proc/sys/vm/max_map_count
# If you want to persist across reboots
echo "vm.max_map_count=9999999" | sudo tee -a /etc/sysctl.conf

```
