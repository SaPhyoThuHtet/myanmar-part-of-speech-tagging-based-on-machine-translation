# Part-of-Speech-Tagging-Based-on-Machine-Translation, NLP-Class-Final-Project
This compares the performances achieved by Phrase-Based Statistical Machine Translation system (PBSMT), Neural Machine Translation based on sequence model of LSTM (Long Short Term Memory), and Attention-Based Neural Machine Translation systems when translating Part-Of-Speech tagging (POS tagging) in Myanmar Language.  Part-Of-Speech tagging is essential in natural language processing: most NLP tasks such as building lemmatizers, text classification, spelling checkers, and others require POS Tagging as a foundation step. The three approaches use parallel data Myanmar-POS tagging corpus with word segmented 10k text. Through the research, PBSMT outperforms NMT. PBSMT also has a much higher evaluation score in comparison. The evaluation process of this research uses metrics RIBES score, BLEU score, and ChrF++. The result shows the Statistical approach outperforms Neural Machine Translation based on the data used in this research.


## Introduction
Part of speech is a category to which a word is assigned by its syntactic functions and so the POS tagging is the activity of marking up a word in a text (corpus) as corresponding to a particular part of speech. Part of Speech tagging (also known as Grammatical tagging) is one of the most important NLP research processes. POS also is an important port in Linguistics. As it has a relationship with adjacent and related words in a phrase, sentence, or paragraph, Part-Of-Speech Tagging stands as a fundamental role in NLP research processes. Myanmar is one of the most spoken languages in Myanmar by the people in plain and also a sub-language for most people of the hills and belongs to the subfamily of Sino-Tibetan languages.
Myanmar is one of the under-resourced languages and there is no exact rule for word boundaries. Myanmar Language also needs to be POS tagged(Grammatical tagging). Like other translations (E.g. English to Spanish), Myanmar and POS tags can use the machine translation approach. Myanmar sentence is input as source language and POS would be the target language. For example,
ဦးသန့် အား ၎င်း မွေးဖွား ရာ ပန်းတနော် မြို့ ကို ရည်စူး ၍ ပန်းတနော် ဦးသန့် ဟု အမည်တွင် ခဲ့ သည် ။
n ppm pron v part n n ppm v conj n n part v part ppm punc

Neural Machine Translation, especially Attention-based models, and Phrase-based Machine Translation both recently become the choices among translate methods. 
In this paper, we focused on both Encoder Decoder Model and also Encoder Decoder with Attention mechanism. 
Statistical methods have normally based on many approaches but choose to perform with a phrase-based mechanism.
Phrase tables mapped one-to-one in parallel. The data texts are word-segmented.
In this paper there are 15 part-of-speech tags for Myanmar Language.


## Data
Datas are from GitHub of Dr.Ye Kyaw Thu. 
Data are segmented and Myanmar-POS tags parallel corpus. 
Maximum words per a sentence is cut to be 150 and left 10k in data sentences. 
Sample of the data can be described as
ပထမ မှာ သားရေ ပေါ် တွင် ကပ် ၍ ပေါက် သော အမွေး နု များ ဖြစ် သည် ။<|||>adj ppm n n ppm v conj v part n adj part v ppm punc
ခရစ်နှစ် ၁၈၈၆ ခုနှစ် တွင် ဘင်္ဂလား ခြေလျင်တပ် မှ ဗိုလ်မှူးကြီး မေ ကို အစွဲပြု ၍ မေမြို့ ဟု ဗြိတိသျှ တို့ က ခေါ်တွင် ခဲ့ သည် ။<|||>n num n ppm n n ppm n n ppm v conj n part n part ppm v part ppm punc

1. abb as Abbreviation (E.g. အ.မ.က, အ.လ.က),
2. adj as Adjective (E.g. ၀သော, ပိန်သော),
3. adv as Adverb (E.g.နှေးနှေး),
4. conj as Conjunction (E.g. နှင့်,  ဖြင့် ),
5. fw as Foreign Word (E.g. 1, 2, Facebook),
6. int as Interjection (E.g. အောင်မလေး),
7. n as Noun (E.g. ကား, နွား),
8. num as Number (E.g. ၁, ၂, ၃),
9. part as Particle (E.g. ပြီး, များ),
10. ppm as Post-positional Marker (E.g. သည်, က, ကို , သို့, မှာ, တွ င် ),
11. pron as Pronoun(E.g. ကျွန်မ, သင်, သူ , သူ မ),
12. punc as Punctuation(E.g. ။, ၊),
13. sb as Symbol(E.g. %, $),
14. tn as Text Number (E.g. တစ်, နှစ်)
15. v as Verb (E.g. လှုပ်ရှား )


