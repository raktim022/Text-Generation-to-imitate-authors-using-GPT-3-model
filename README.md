# Text-Generation-to-imitate-authors-using-GPT-3-model

This code is written to use a GPT-3(DPT Neo with 1.3 billion parameters) model to generate text from some of my favourite books and check how closely the model generates text that closely resembles the author.

After importing and installing PyTorch and transformers, I have imported pipeline from transformers.
Then I have downloaded and initialized the GPT model with 1.3 billion parameters, with sampling set at True and temperature=0.9. I could have used the version with 2.7 billion parameters, but my system kept crashing.
I ttok my input as a '.txt' file. I fed the model with the first 200 words, and then made it generate the next 800 words.
After cleaning the generated text, I extracted the actual 800 words from the original text and compared the two using Jaccard similarity, i.e., ratio of words they have in common to words they have in their union.


After testing the code with texts extracted from "And Then There Were None" by Agatha Christie, "A Wind-Up Bird Chronicle" by Haruki Murakami,
and "Rules for Perfect Murders" by Peter Swanson, I found that the model generated texts which was 22% similar to original text of Agatha Christie,
27% similar to that of Murakami and 23% to that of Peter Swanson.

<b>Conclusion</b> \\
This percentage could have been higher if a model with a larger number of parameters were used and a input of a higher size was used for text generation.
