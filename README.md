This will go over the simple steps in clearing a Proxmox VE node that was previously connected to a Proxmox Datacenter Manager host so it can be connected to a new one.

Use the following command to list the current tokens

```
pveum user token list root@pam
```

<img width="975" height="133" alt="image" src="https://github.com/user-attachments/assets/d7c8db12-98fa-4845-906d-ce8cf7eae9cf" />


The tokenid indicates what token was generated previously for this, DCM = Data Center Manager

Remove the “link” from the DCM node in the VE node

The following command will be used to remove the token from your VE node

```
pveum user token delete root@pam <your token id>
```

<img width="975" height="186" alt="image" src="https://github.com/user-attachments/assets/02564623-c052-4fc3-81a1-06335efadf5e" />


Notice now that when I list tokens on the VE node, the original one is gone.

Now you can go forward adding it to your new Datacenter Manager node. 
