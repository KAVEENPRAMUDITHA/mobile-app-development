-----------------------------important shell codes--------------------------------------------------------------



create env====>



conda create -n intelligent\_systems\_exam  --offline -y



conda activate intelligent\_systems\_exam



conda install ipykernel



python -m ipykernel install --user --name intelligent\_systems\_exam --display-name "Python (intelligent\_systems\_exam)"





-----------------------------------------library install-----------------------------------------------------------



conda install pandas





pip install pandas numpy scikit-learn nltk keras tensorflow matplotlib seaborn wordcloud langchain-community



conda install transformers

pip install tf-keras

pip install wordcloud





conda install pandas numpy scikit-learn matplotlib seaborn -y



pip install nltk keras tensorflow wordcloud langchain-community



conda activate intelligent\_systems\_exam







!pip install spacy



!python -m spacy download en\_core\_web\_sm



pip install langdetect











pip show setuptools



jupyter kernelspec list



jupyter kernelspec remove new-conda-env



jupyter notebook



!jupyter nbconvert --execute --to html --stdout "intelligent\_systems\_examination\_notebook.ipynb"









============================================================================================================================================================



Scikit-learn Pipeline and ColumnTransformer---->[scikit learn pipline](https://www.freecodecamp.org/news/machine-learning-pipeline/)

Spacy ----> [spacy](https://www.freecodecamp.org/news/getting-started-with-nlp-using-spacy/) ,[ tutorial](https://www.analyticsvidhya.com/blog/2020/03/spacy-tutorial-learn-natural-language-processing/)

Sentiment Analysis ---->[Sentiment Analysis using VADER](https://medium.com/@rslavanyageetha/vader-a-comprehensive-guide-to-sentiment-analysis-in-python-c4f1868b0d2e),[ Twitter Sentiment Analysis using Python](https://www.freecodecamp.org/news/tweet-sentiment-analysis-python/), [Sentiment Analysis kaggel](https://www.kaggle.com/code/niraliivaghani/sentiment-analysis-using-vader), [vader tutorial](https://www.analyticsvidhya.com/blog/2022/10/sentiment-analysis-using-vader/)



1\. Bag-of-Words (BoW) 🛍

මොකක්ද: Text එකක් දිහා බලන සරලම ක්‍රමයක්. හරියට වාක්‍යයක් වචන දාපු බෑග් එකක් වගේ සලකනවා.



කරන්නේ: ඒ බෑග් එකේ තියෙන හැම වචනයක්ම කී පාරක් තියෙනවද කියලා ගණන් කරනවා විතරයි.



ගණන් ගන්නේ නැත්තේ: වචන වල පිළිවෙල, ව්‍යාකරණ, වචන වල සැබෑ තේරුම (context).



උදාහරණය: "බෙහෙත් හොඳ නැහැ" සහ "බෙහෙත් නරක නැහැ" කියන දෙකම BoW වලට ගොඩක් දුරට සමානයි, මොකද "බෙහෙත්" සහ "නැහැ" කියන වචන දෙකම තියෙනවා. "නරක" ද "හොඳ" ද කියන එකේ වෙනස තේරෙන්නේ නැහැ.



ප්‍රයෝජනය: සරල text classification වැඩ වලට මූලික පියවරක් විදියට. වේගවත්.



අවාසිය: භාෂාවේ සියුම් තැන් (nuance) තේරුම් ගන්න බැහැ.



2\. VADER (Valence Aware Dictionary and sEntiment Reasoner) 📖⚖

මොකක්ද: විශේෂයෙන්ම සමාජ මාධ්‍ය (social media) වල තියෙන sentiment (හැඟීම) හොයන්න හදපු, rule-based (නීති මත පදනම් වූ) ක්‍රමයක්.



කරන්නේ: එයා ළඟ වචන dictionary එකක් තියෙනවා, ඒකේ හැම වචනෙකටම sentiment score එකක් දීලා තියෙනවා (e.g., "good" = +3, "bad" = -3).



BoW වලට වඩා දියුණුයි: VADER, BoW වගේ නිකන් වචන ගණන් කරන්නේ නැහැ. ඒක මේ දේවලුත් බලනවා:



Punctuation: "!!!" වගේ දේවල් දැම්මම sentiment එකේ තීව්‍රතාවය (intensity) වැඩි කරනවා.



Capitalization: "GREAT" වගේ capital අකුරු දැම්මමත් intensity එක වැඩි කරනවා.



Negation: "not good" වගේ ඒවා අඳුනගෙන, score එක අනිත් පැත්ත හරවනවා.



ප්‍රයෝජනය: Social media posts, reviews වගේ කෙටි text වල sentiment එක ඉක්මනට හොයාගන්න හොඳයි. Train කරන්න දෙයක් නැහැ.



අවාසිය: Dictionary එකේ නැති අලුත් වචන/slang වල තේරුම දන්නේ නැහැ. සංකීර්ණ වාක්‍ය වල context එක සමහරවිට මඟහැරෙන්න පුළුවන්.



3\. BERT (Bidirectional Encoder Representations from Transformers) 🧠📚

මොකක්ද: මේක විශාල, දියුණු, pre-trained neural network model එකක් (Transformer architecture එකක්). හරියට භාෂාවක් ගැන ගොඩක් දේවල් ඉගෙනගත්ත "මොළයක්" වගේ.



කරන්නේ: BoW සහ VADER වගේ වචන දිහා තනි තනියෙන් බලන්නේ නැතුව, BERT වාක්‍යයක තියෙන හැම වචනයක්ම, ඒකට ඉස්සරහින් සහ පස්සෙන් තියෙන වචනත් එක්ක සලකලා බලනවා. ඒ කියන්නේ, ඒක සන්දර්භය (context) තේරුම් ගන්නවා.



Bidirectional (දෙපැත්තටම බලන): "Bank" කියන වචනේ තේරුම ("river bank" ද "money bank" ද?) තීරණය කරන්නේ ඒ වචනෙට ඉස්සරහින් තියෙන වචන වගේම, පස්සෙන් තියෙන වචනත් බලලයි.



Pre-trained: Google එකෙන් මුළු Internet එකේම වගේ text (Wikipedia, books) කියවලා මේ model එක train කරලා තියෙන්නේ. ඒ නිසා ඒකට භාෂාව ගැන ලොකු දැනුමක් තියෙනවා.



Fine-tuning: අපිට මේ ලොකු model එක අරගෙන, අපේම පොඩි dataset එකකින් තව ටිකක් train කරලා (fine-tune), අපේම විශේෂ වැඩකට (sentiment analysis, classification, question answering) හුරු කරගන්න පුළුවන්.



ප්‍රයෝජනය: ඉතාමත්ම දක්ෂයි. Context, nuance හොඳට තේරෙනවා. Sentiment analysis වලට විතරක් නෙවෙයි, NLP වැඩ ගොඩකට පාවිච්චි කරන්න පුළුවන්.



අවාසිය: අනිත් ක්‍රම දෙකට වඩා ගොඩක් ලොකුයි. වැඩ කරන්න වැඩි computer power එකක් (විශේෂයෙන් GPU) ඕන වෙනවා. ටිකක් slow වෙන්න පුළුවන්.

