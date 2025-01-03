# 100 - Add Nodes to Workflow

Right-click on the canvas and choose ```Add Node > loaders > Load Checkpoint```.

![comfyai_new_workflow_002](https://github.com/user-attachments/assets/92748e1b-f8d1-425c-a5f7-4cd604be647f)

We change the model to **Dream-Shaper-8.safetensors** by clicking on the arrows inside of our new Node **Load Checkpoint**.

![comfyai_new_workflow_003](https://github.com/user-attachments/assets/b18c6380-8d1c-4121-b733-c18747c73cef)

Zoom out a bit so you have enough space for adding more nodes. Next, click on the yellow dot next to **Clip** on the **Load Checkpoint** Node and drag it to the right and let go. A new **CLIP** menu pops up. Select **CLIPTextEncode** as this will contain our Prompt soon.

![comfyai_new_workflow_004](https://github.com/user-attachments/assets/6cb9934b-b92d-42b5-8088-6a0e0abda92d)

The new Node called **CLIP Text Encode (Prompt)** we'll rename to **CLIP Text Encode (Positive)** as it will contain our Positive Prompt soon.

![comfyai_new_workflow_005](https://github.com/user-attachments/assets/17e92d89-02ab-4743-8f7c-fe582d07b334)

Add the prompt: **A box of stones** (just as an example) inside the CLIP Text Encode (Positive) node.

![comfyai_new_workflow_006](https://github.com/user-attachments/assets/21771e7d-acc3-4544-aee9-a2e50aa7e3a9)

Repeat the node creation but now rename it to **CLIP Text Encode (Negative)** and add the prompt **A bag of noodles** (just as a contrary example).

![comfyai_new_workflow_007](https://github.com/user-attachments/assets/a308a639-2de0-4513-8151-105f0c546511)

By right-clicking on the node, we can change its color. We'll color the **Positive** node **green**, and the **Negative** node **red** for ease of reference.

![comfyai_new_workflow_008](https://github.com/user-attachments/assets/107ebb05-7c96-49d1-a3ff-c7d82b86dd50)

Next, click on the yellow dot next to **CONDITIONING** on the ```CLIP Text Encode (Positive)``` node and drag it to the right and let go. The **CONDITIONING** menu pops up and we'll choose **KSampler**.

![comfyai_new_workflow_009](https://github.com/user-attachments/assets/e8b4d0ef-3113-4e33-a3f2-42d6470c3f32)

Drag the lines from the CONDITIONING dots of each **CLIP** node to their respective input dots. Hence, CLIP Text Encode (Positive) to **positive** of KSampler, and CLIP Text Encode (Negative) to **negative** of KSampler.

![comfyai_new_workflow_010](https://github.com/user-attachments/assets/6a3d25a0-d1e5-4d37-8a1a-44501a21502b)

Next, connect the **MODEL** purple dot from the **Load Checkpoint** node to the **model** purple dot in the **KSampler** node, like so:

![comfyai_new_workflow_011](https://github.com/user-attachments/assets/68feb9ef-6b86-4080-849d-fe11b41007ca)

Moving on, we drag a line from the pink dot next to **latent_image** in the **KSampler** node and drop it somewhere below on the canvas. The **LATENT** menu pops up and we choose **EmptyLatentImage**.

![comfyai_new_workflow_012](https://github.com/user-attachments/assets/603686b5-e0d0-417e-8548-08a9e0541666)

The **Empty Latent Image** node shows the **image size** that we will start with, here **512** pixels **width** by **512** pixels **height** and we'll be creating **1** image at a time (i.e. **batchsize** = 1):

![comfyai_new_workflow_013](https://github.com/user-attachments/assets/d2a5cd23-e3a7-4fde-9819-8a2cb11eed16)

Now we'll drag a line from the **LATENT** purple dot in the **KSampler** node to the right and let go. A **LATENT** menu pops up where we select **VADecode**:

![comfyai_new_workflow_014](https://github.com/user-attachments/assets/f7f373b8-2b2e-42fc-8754-40c0b1a7a683)

Make sure the connection is actually made:

![comfyai_new_workflow_015](https://github.com/user-attachments/assets/498e746e-2813-446a-8aa4-2f9237964154)



MORE ...
