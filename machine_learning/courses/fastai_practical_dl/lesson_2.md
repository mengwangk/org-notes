# Lesson 2 - Evidence and p values

- Overfitting is the single most important and challenging issue.

## Transfer Learning
Using a pretrained model for a task different to what is was originally trained
for.

*Fine tuning* - a transfer learning technique where the weights of a pretrained
model are updated by training for additional epochs using a different task to
that used for pretraining.

### Pre-trained models
- Model zoo

## State of Deep Learning
- Vision - detection classification
- Text - classification, conversation
- Tabular - high cardinality; GPU (Rapids)
- Recys - prediction <> recommendation
- Multi-modal - labeling;captioning; human in the loop
- Others - NLP->Protein

Paper - high temperature and high humidity reduce transmission of Covid-19

> Effective Reproduction Number
> $$ R_0 $$ 

## How might we decide if there's a relationship
- Pick a "null hypothesis", e.g. "no relationship"
- Gather data of independent & dependent variables - temperature & R
- What % of time would we see that relationship by chance?

P-value = is a probability of an observed (or more extreme) resut assuming that the null hypothesis is true.

The p value is the evidence against a null hypothesis. The smaller the
p-value, the stronger the evidence that you should reject the null
hypothesis. P values are expressed as decimals although it may be easier
to understand what they are if you convert them to a percentage. For
example, a p value of 0.0254 is 2.54%.

- P-value does not measure probability that the hypothesis will be true.
- P-value does not measure importance of results.
.... Refer to American Statistical Association

Designing great data products - Oreilly
Strategy->Data->Analytics->Implementation->Maintenance
<---- Identify and manage constraints ------->

Consider the utility of all possibility
- No relationship - act as if there was - RED
- Is real relationship - acts as if there was
- No real relationship. Don't acts as if there was
- Is real relationship. Don't act as if there was - RED

Prior belief?

Bing Image Search - download and create dataset.

