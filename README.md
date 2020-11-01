# Adding-SSH-to-Github
Adding SSH key to github using Git bash on windows machine.


1. Open Git Bash.

2. Paste the text below, substituting in your GitHub email address.

   > $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   
3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
   
   > Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]
   
4. At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".

   > Enter passphrase (empty for no passphrase): [Type a passphrase]
   
   > Enter same passphrase again: [Type passphrase again]
  
5. Ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in "Working with SSH key passphrases", or start it manually:

    > $ eval $(ssh-agent -s)
    
 6. Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in       the command with the name of your private key file.

    > $ ssh-add ~/.ssh/id_rsa
   
 7. Copy the SSH key to your clipboard.

    If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or        whitespace.

    > $ clip < ~/.ssh/id_rsa.pub
    
    
# REFERENCE
https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
