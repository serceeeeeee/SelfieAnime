Converting selfies into anime-style portraits is popular in social media and games. Anime avatars
allow users to express identity in a stylized, privacy-preserving way, but commercial filters are
proprietary and simple image filters often fail to preserve facial structure or avoid artifacts (e.g.,
“cracks” on the skin, distorted eyes).
In this project I study unpaired selfie-to-anime translation: given a real selfie as input, the goal is
to generate an anime portrait that (i) preserves the person’s facial layout and identity, (ii) adopts
anime-like colors and line art, and (iii) avoids strong artifacts. The data are unpaired: I have separate
collections of selfies and anime faces, but no one-to-one correspondence. This makes a standard
supervised regression approach impossible.
Generative adversarial networks (GANs), and in particular CycleGAN, are well-suited to unpaired
image-to-image translation. I build on CycleGAN and propose several modifications: resize-
convolution upsampling to reduce checkerboard artifacts , spectral-normalized PatchGAN
discriminators, and VGG-based content loss plus total-variation (TV) loss to preserve facial
structure and smooth shading. Experiments show that these changes produce cleaner, more coherent
anime faces and significantly reduce the “half-animated” and cracked-skin failure modes observed in
early experiments.
