#    

FAAC: Facial Animation Generation with Anchor Frame and Conditional Control for Superior Fidelity and Editability
=================================================================================================================

FAAC
----

![main figure](./FAAC_main_fig.png)

Abstract
--------

Over recent years, diffusion models have facilitated significant advancements in video generation. Yet, the creation of face-related videos still confronts issues such as low facial fidelity, lack of frame consistency, limited editability and uncontrollable human poses. To address these challenges, we introduce a facial animation generation method that enhances both face identity fidelity and editing capabilities while ensuring frame consistency. This approach incorporates the concept of an anchor frame to counteract the degradation of generative ability in original text-to-image models when incorporating a motion module. We propose two strategies towards this objective: training-free and training-based anchor frame methods. Our method's efficacy has been validated on multiple representative DreamBooth and LoRA models, delivering substantial improve ments over the original outcomes in terms of facial fidelity, text-to-image editability, and video motion. Moreover, we introduce conditional control using a 3D parametric face model to capture accurate facial movements and expressions. This solution augments the creative possibilities for facial animation generation through the integration of multiple control signals.

🎬   Personalized Facial Animation   🎬
=======================================

For best and full view, please refer to the folder ```FAAC_results/main_results```.

 We select four representative LoRA character and perform personalized facial animation.  Each line represents a different LoRA character (from top to bottom:  Liam Neeson, Asian Girl, Suriya Sivakumar, Angelina Joile). For each LoRA character, we have employed three prompts to generate facial animations. The prompt corresponding to each video clip is annotated below it. Our FAAC works effectively and generate frame-consistent results on diverse characters and prompts. Moreover, two advantages of FAAC can be reflected in the above results: (1) face identity fidelity (2) editing capabilities by text prompts. Due to our key-frame strategy, we can better maintain fidelity to characters and text prompt, without being compromised by the motion module.

| Character        | Result - 1                                                   | Result - 2                                                   | Result - 3                                                   |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Liam Neeson      | ![](./FAAC_results/main_results/LiamNeeson/A%20close-up%20of%20a%20guy%20with%20a%20relaxed%20and%20easygoing%20expression.gif) | ![](./FAAC_results/main_results/LiamNeeson/A%20man%2C%20wearing%20a%20hat%2C%20against%20a%20beach%20background.gif) | ![](./FAAC/tree/main/FAAC_results/main_results/LiamNeeson/A%20man%20with%20a%20confident%20and%20charismatic%20smile%2C%20making%20eye%20contact%20with%20the%20camera.gif) |
|                  | **A close-up shot of a guy with a relaxed and easygoing expression** | **A man, wearing a hat, against a beach background**         | **A man with a confident smile, making eye contact with the camera** |
| Asian Girl       | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/AsianGirl/A%20portrait%20of%20a%20woman%20in%20a%20natural%20setting%2C%20wearing%20a%20headband.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/AsianGirl/A%20close-up%20shot%20of%20a%20girl%20with%20glasses%20and%20earrings.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/AsianGirl/A%20girl%20adorned%20with%20a%20colorful%20tattoo%20on%20the%20cheek.gif) |
|                  | **A portrait of a woman in a natural setting, wearing a headband** | **A close-up shot of a girl with glasses and earrings**      | **A girl adorned with a colorful tattoo on the cheek**       |
| Suriya Sivakumar | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/Suriya/A%20man%20with%20a%20goatee%20and%20a%20leather%20cowboy%20hat.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/Suriya/A%20man%20with%20a%20goatee%20and%20a%20piercing%20gaze%2C%20against%20a%20backdrop%20of%20mountain%20peaks.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/Suriya/A%20man%20with%20a%20surprised%20and%20delighted%20expression%2C%20showcasing%20a%20moment%20of%20unexpected%20joy.gif) |
|                  | **A man with a goatee and a leather cowboy hat**             | **A man with a piercing gaze against a backdrop of mountain peaks** | **A man with a surprised and delighted expression, showcasing a moment of unexpected joy** |
| Angelina Joile   | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/AngelinaJoile/a%20beautiful%20woman%20starts%20to%20talk%2C%20bright%2C%20beautiful%20face%2C%20realistic%2C%20solo.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/AngelinaJoile/a%20close-up%20of%20a%20woman%20with%20elegant%20pearl%20earrings%20and%20a%20vintage%20hairstyle.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/main_results/AngelinaJoile/a%20close-up%20shot%20of%20a%20woman%20with%20vibrant%2C%20multicolored%20hair.gif) |
|                  | **A beautiful woman starts to talk, bright, beautiful face, realistic, solo** | **A close-up shot of a woman with elegant pearl earrings and a vintage hairstyle** | **A close-up shot of a woman with vibrant, multicolored hair** |

🎞   Control Results   🎞
=========================

For best and full view, please refer to the folder ```FAAC_results/control_results```.

We demonstrate our FAAC-with-control results.  We select four representative driving templates, including  common facial movements such as opening the mouth, blinking, turning the head, and their combinations. Each line represents a different driving template. Then we use the driving template to control the facial animation results, assisted by the text prompt. The specific control method is mentioned in the paper.  The text prompt corresponding to each video clip is annotated below it. The above results indicate that we can generate controllable facial animations with targeted motion patterns.

|              |                                                              | Result - 1                                                   | Result - 2                                                   |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Template - 1 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/1/driving_template.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/1/a%20close-up%20shot%20of%20a%20woman%20with%20vibrant%2C%20multicolored%20hair.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/1/A%20man%20with%20a%20goatee%20against%20a%20backdrop%20of%20mountain%20peaks.gif) |
|              | **Driving Template**                                         | **a close-up shot of a woman with vibrant, multicolored hair** | **A man with a goatee against a backdrop of mountain peaks** |
| Template - 2 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/2/driving_template.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/2/a%20woman%2C%20elegant%20angel%2C%20crown%20on%20the%20head%2C%20wings%20on%20the%20back%2C%20in%20a%20floral%20garden%20setting.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/2/A%20portrait%20of%20a%20face%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) |
|              | **Driving Template**                                         | **a woman, elegant angel, crown on the head, wings on the back, in a floral garden setting** | **A portrait of a face against a brick wall, wearing a bandana** |
| Template - 3 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/3/driving_template.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/3/A%20portrait%20of%20a%20man%20with%20a%20goatee%2C%20wearing%20a%20plaid%20shirt%20and%20surrounded%20by%20autumn%20leaves.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/3/A%20portrait%20of%20a%20face%20against%20a%20graffiti-covered%20wall%2C%20wearing%20a%20necklace.gif) |
|              | **Driving Template**                                         | **A portrait of a man with a goatee, wearing a plaid shirt and surrounded by autumn leaves** | **A portrait of a face against a graffiti-covered wall, wearing a necklace** |
| Template - 4 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/4/driving_template.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/4/A%20girl%20is%20smiling%2C%20bright%2C%20beautiful-face%2Crealistic%2Csolo.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/control_results/4/A%20portrait%20of%20a%20guy%20with%20a%20handlebar%20mustache%2C%20wearing%20a%20vintage%20pilot's%20jacket.gif) |
|              | **Driving Template**                                         | **A girl is smiling, bright, beautiful-face,realistic,solo** | **A portrait of a guy with a handlebar mustache, wearing a vintage pilot's jacket** |

## Some Additional Results For Rebuttal

 ### Range of Motion

Even without additional control, the video clips we generate possess dynamism, including the movement of characters and changes in camera perspective. We present more examples when our method exhibits a greater range of motion compared to other approaches under the same prompt, LoRA, DreamBooth and so on.

|                | AnimateDiff                                                  | FAAC (Our Method)                                            |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Comparison - 1 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%201/AnimateDiff-A%20portrait%20of%20a%20girl%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%201/FAAC-A%20portrait%20of%20a%20girl%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) |
|                | **A portrait of a girl against a brick wall, wearing a bandana** | **A portrait of a girl against a brick wall, wearing a bandana** |
| Comparison - 2 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%202/AnimateDiff-A%20portrait%20of%20a%20girl%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%202/FAAC-A%20portrait%20of%20a%20girl%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) |
|                | **A portrait of a girl against a brick wall, wearing a bandana** | **A portrait of a girl against a brick wall, wearing a bandana** |
| Comparison -3  | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%203/AnimateDiff-a%20woman%2C%20tilt%20her%20head%2C%20wearing%20a%20hat%2C%20against%20a%20beach%20background.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%203/FAAC-a%20woman%2C%20tilt%20her%20head%2C%20wearing%20a%20hat%2C%20against%20a%20beach%20background.gif) |
|                | **a woman, tilt her head, wearing a hat, against a beach background** | **a woman, tilt her head, wearing a hat, against a beach background** |
| Comparison - 4 | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%204/AnimateDiff-A%20man%20with%20a%20confident%20and%20charismatic%20smile%2C%20making%20eye%20contact%20with%20the%20camera.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%204/FAAC-A%20man%20with%20a%20confident%20and%20charismatic%20smile%2C%20making%20eye%20contact%20with%20the%20camera.gif) |
|                | **A man with a confident and charismatic smile, making eye contact with the camera** | **A man with a confident and charismatic smile, making eye contact with the camera** |
| Comparison -5  | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%205/AnimateDiff-A%20man%20with%20a%20confident%20and%20charismatic%20smile%2C%20making%20eye%20contact%20with%20the%20camera.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Range_of_Motion/comparison%20-%205/FAAC-A%20man%20with%20a%20confident%20and%20charismatic%20smile%2C%20making%20eye%20contact%20with%20the%20camera.gif) |
|                | **A man with a confident and charismatic smile, making eye contact with the camera** | **A man with a confident and charismatic smile, making eye contact with the camera** |

### fine-grained control of facial expressions

We demonstrate that our method provides more fine-grained control over facial expressions, such as improved control over **blinking eyes**. This is reflected in two aspects: 

(1) Achieving better facial expression editing solely through prompts, without the need for additional control modules. 

(2) Utilizing additional control modules to achieve a more controllable outcome.

|                                                    | AnimateDiff                                                  | FAAC (Our Method)                                            |
| -------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Comparison - 1<br />(edit eyes by prompts)         | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Fine-grained_Facial_Expression/comparison%20-%201/Animatediff-A%20close-up%20shot%20of%20a%20man%20with%20a%20mischievous%20grin%20and%20raised%20eyebrows.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Fine-grained_Facial_Expression/comparison%20-%201/FAAC_A%20close-up%20shot%20of%20a%20man%20with%20a%20mischievous%20grin%20and%20raised%20eyebrows.gif) |
|                                                    | A close-up shot of a man with a mischievous grin and **raised eyebrows** | A close-up shot of a man with a mischievous grin and **raised eyebrows** |
| Comparison - 2 <br />(edit eyes by control signal) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Fine-grained_Facial_Expression/comparison%20-%202/AnimateDiff%20-A%20portrait%20of%20a%20girl%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) | ![](https://github.com/Paper-FAAC/FAAC/tree/main/FAAC_results/compare_results/Fine-grained_Facial_Expression/comparison%20-%202/FAAC-A%20portrait%20of%20a%20girl%20against%20a%20brick%20wall%2C%20wearing%20a%20bandana.gif) |
|                                                    | A portrait of a girl against a brick wall, wearing a bandana | A portrait of a girl against a brick wall, wearing a bandana<br />**+ a blinking eyes driving template** |

