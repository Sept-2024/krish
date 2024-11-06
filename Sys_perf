#!/bin/bash

echo "CPU Utilization"
mpstat 1 1 | awk 'NR==4 {print "Average CPU Usage: " 100-$NF "%"}'

echo ""
echo "Memory Utilization"
free -m | awk 'NR==2 {printf "Used Memory: %s MB (%.2f%%)\n", $3, ($3/$2)*100}'

echo ""
echo "Disk Utilization"
df -h | awk '{print$5}' | sed -n 2p

echo "System Perforamnce Checked"
echo ""
