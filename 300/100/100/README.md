# 100 - Add Nodes to Workflow

Right-click on the canvas and choose ```Add Node > loaders > Load Checkpoint```.

![comfyai_new_workflow_002](https://github.com/user-attachments/assets/92748e1b-f8d1-425c-a5f7-4cd604be647f)

We change the model to **Dream-Shaper-8.safetensors** by clicking on the arrows inside of our new Node **Load Checkpoint**.

![comfyai_new_workflow_003](https://github.com/user-attachments/assets/b18c6380-8d1c-4121-b733-c18747c73cef)

Zoom out a bit so you have enough space for adding more nodes. Next, click on the yellow dot next to **Clip** on the **Load Checkpoint** Node and drag it to the right and let go. A new Clip Dialogue pops up. Select **CLIPTextEncode** as this will contain our Prompt soon.

![comfyai_new_workflow_004](https://github.com/user-attachments/assets/6cb9934b-b92d-42b5-8088-6a0e0abda92d)

The new Node called **CLIP Text Encode (Prompt)** we'll rename to **CLIP Text Encode (Positive)** as it will contain our Positive Prompt soon.

![comfyai_new_workflow_005](https://github.com/user-attachments/assets/17e92d89-02ab-4743-8f7c-fe582d07b334)

Add the prompt: **A box of stones** (just as an example) inside the CLIP Text Encode (Positive) node.

![comfyai_new_workflow_006](https://github.com/user-attachments/assets/21771e7d-acc3-4544-aee9-a2e50aa7e3a9)

Repeat the node creation but now rename it to **CLIP Text Encode (Negative)** and add the prompt **A bag of noodles** (just as a contrary example).

![comfyai_new_workflow_007](https://github.com/user-attachments/assets/a308a639-2de0-4513-8151-105f0c546511)

MORE ...