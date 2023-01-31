*To create new SSH key:* \
ssh-keygen -t ed25519 -C "aylaj@reed.edu" \
hit enter for default file location, & make password

*To start SSH agent & add key to agent:* \
eval "$(ssh-agent -s)" \
ssh-add ~/.ssh/id_ed25519 (ed_xxxxx is the name of key, should be shown from output of ssh-keygen above)

(or to create another key: ssh-keygen -t rsa -C "alanrjes@gmail.com" -f "alanrjes", and to view: cat ~/.ssh/alanrjes.pub)

*To view public key:* \
cat ~/.ssh/id_ed25519.pub (copy this output)

*To add SSH key to github account:* \
In Github go to Settings, under "Access" find "SSH and GPG keys", and paste public key into key field.

*To test SSH connection:* \
ssh -T git@github.com

*To clone empty repository:* \
git clone git@github.com:alwritescode/cs351-version-control-la.git

*To add file to repository:* \
create file in editor and save \
git add test-file.txt

*To commit and push*: \
git commit -m "step 5, partner A adds and commits a file" \
git push

*Step 11, result of git push:* \
"To github.com:alwritescode/cs351-version-control-la.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:alwritescode/cs351-version-control-la.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details."

*Step 12:* \
git add test-file.txt \
git commit -M "step 12" \
git push

*Step 15:* \
git branch newBranchA \
git checkout newBranchA

*Step 18:* \
git checkout newBranchA \
git merge ella-step15 \
git push \
(partner A's file was added to branch B)
