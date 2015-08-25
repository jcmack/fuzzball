How to Enable Syntax Highlighting in Nano


'''
touch ~/.nanorc
for x in `ls /usr/share/nano/`; do echo "include /usr/share/nano/$x" >> ~/.nanorc; done
'''
