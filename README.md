1)Question: Bash Sript Digit transformation given a string of random length replace all numeric characters with asterisk character.
solution: #!/bin/bash

# Input string
my_variable="The number is 12345"
# Replace numeric characters with asterisks
result=$(echo "$my_variable" | sed 's/[0-9]/\*/g')
# Output the result
echo "The result is \"$result\""


2)Question: Complete the script at "/home/ubuntu/894899-linux-access-log-filtering/script.sh" to extract an archive,
filter logs for 5xx status codes with non-"127.0.0.1" IPs, and save results to "/tmp/access.log" using "sudo solve"
Solution:
cd /home/ubuntu/894899-linux-access-log-filtering
# Extract the archive
tar -xzf archive.tar.gz
# Find records with status code 5xx and non-matching IP addresses
grep -E '^[^ ]+ [^ ]+ [^ ]+ \[([^\]]+)\] "[^"]+" [5-9][0-9][0-9] [0-9]+' /.log | grep -v ' 127.0.0.1 ' > /tmp/access.log
# Output success message
echo "Logs filtered and saved to /tmp/access.log


3)Question: Python Implement the function even(start, n) which returns a list of the n smallest even integers greater than or equal to start, in ascending order.
Constraints: 1 ≤ start, n ≤ 100 
Solution: 
def even(start, n):
    result = [num for num in range(start, start + 2 * n, 2)]
    return result

if _name_ == "_main_":
    start, n = map(int, raw_input().split())
    output = even(start, n)
    print ' '.join(map(str, output))
    
