# 100 - Add Nodes to Workflow

Right-click on the canvas and choose ```Add Node > loaders > Load Checkpoint```.

![comfyai_new_workflow_002](https://github.com/user-attachments/assets/92748e1b-f8d1-425c-a5f7-4cd604be647f)

We change the model to **Dream-Shaper-8.safetensors** by clicking on the arrows inside of our new Node **Load Checkpoint**.

![comfyai_new_workflow_003](https://github.com/user-attachments/assets/b18c6380-8d1c-4121-b733-c18747c73cef)

Zoom out a bit so you have enough space for adding more nodes. Next, click on the yellow dot next to **Clip** on the **Load Checkpoint** Node and drag it to the right and let go. A new Clip Dialogue pops up. Select **CLIPTextEncode** as this will contain our Prompt soon.

![comfyai_new_workflow_004](https://github.com/user-attachments/assets/6cb9934b-b92d-42b5-8088-6a0e0abda92d)

The new Node called **CLIP Text Encode (Prompt)** we'll rename to **CLIP Text Encode (Positive)** as it will contain our Positive Prompt soon.

![comfyai_new_workflow_005](https://github.com/user-attachments/assets/17e92d89-02ab-4743-8f7c-fe582d07b334)




MORE ...
