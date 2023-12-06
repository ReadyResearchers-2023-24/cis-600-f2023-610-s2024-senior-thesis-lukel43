# Template description

This repository contains the starter materials for your thesis in Computer
Science 600 and 610 in Fall 2022  and Spring 2023 academic term. The main
directory of this repository contains the Markdown template for a project that
is designed for use with GitHub Classroom. To learn more about the course
in which these assignments were completed, please refer to the `README.md` file.

The template specifies various settings in the `config.yaml` file included in the
repository. Change the appropriate values under the `Project-specific values`
heading. Changing other values outside of that section may cause the project to
fail to build. **Modify these values at your own risk.**

Author your thesis in the `thesis.md` document using appropriate Markdown
hierarchy and syntax; GitHub Actions will automatically create a PDF from the
`abstract.md` and `proposal.md` files. Consult the `README` of the proposal
repository to learn how to properly build and release this PDFs.

## Citations and references

Including references throughout requires a specific pseudo-Markdown tag, demonstrated
in the following blockquote. (Inspect the `thesis.md` file to see the format.)

> A citation, when included correctly, will appear as it does at the end of this
> sentence. [@plaat1996research]

## Labeling figures

To label a figure (i.e. an image), referencing the image using correct Markdown
will automatically caption the figure:

```markdown
![Label](images/IMAGE_NAME.png)
```

## Labeling tables

To provide a label for a table, write a short caption for the table and prefix the caption
with `Table:` as in the example below:

```
Table: A two-row table demonstrating tables

|Row number | Description |
|:----------|:------------|
|1          |Row 1        |
|2          |Row 2        |
```

## Other template information

Two things specific to this template to also keep in mind:

1. It is your responsibility to remove this description section before building
the PDF version you plan to defend.
2. References _will only appear if cited correctly_ in the text

## Note on `LaTeX` commands

Documents may include specific `LaTeX` commands _in Markdown_. To render these, surround the commands
with markup denoting `LaTeX`. For example:

```
Checkmark character:   $\checkmark$
Superscript character: $^{\dag}$
```

If using a special package not included in the template, add the desired `LaTeX`
package or command/macro to the `header-includes` property in [config.yaml](config.yaml).

Should this package not be included in the environment shipped with this template,
you may also need to add the package to the [GitHub Actions Workflow](.github/workflows/main.yml).

Direct any questions about issues to your first reader.

# Introduction

This thesis presents a detailed study and development of an application focused on sports betting odds, with an emphasis on identifying, optimizing, and notifying users about hedging opportunities. Hedging in sports betting involves placing wagers on both outcomes of a binary betting option to ensure a profit, irrespective of the final result. Such opportunities are found when the odds are structured so that the total payout exceeds the sum wagered.

## Motivation

The impetus behind this research stems from two principal aims. The first is to analyze whether an algorithm-based approach to sports betting can enhance user profitability. This involves creating a systematic method for bettors to access comprehensive information, thereby reducing potential losses and mitigating betting risks. The second aim is to contribute to the body of knowledge in sports betting by conducting a historical analysis of betting odds. This part of the research aims to provide insights into the mechanics and strategic use of hedging bets. The overarching goal is to offer a tool that not only aids bettors in making more informed decisions but also helps in curbing the adverse effects of gambling, such as addiction and financial losses.

## Current State of the Art

The landscape of sports betting research, particularly in the context of hedging strategies, is currently limited. Most of the available literature is focused on markets outside the United States, or it concentrates on predicting outcomes of sports events and identifying bets with favorable odds. This thesis distinguishes itself by not predicting outcomes or assessing odds fairness. Instead, it focuses on presenting users with profitable betting options based on current market conditions and data from the-odds-api. A significant aspect of this research is the historical analysis of sports betting odds, an area that has not been thoroughly explored in existing literature. This analysis extends beyond theoretical models, providing a practical examination of historical outcomes and trends in sports betting odds.

## Goals of the Project

The thesis is structured around two primary objectives. The first is a comprehensive historical analysis to ascertain the occurrence and profitability of hedging opportunities in comparison to traditional betting strategies. This involves a systematic examination of past betting data to identify patterns and trends that could inform future betting strategies. The second objective is the development of an application that leverages this historical data to identify and notify users of hedging opportunities as they arise in real-time.

The historical analysis portion of the thesis is critical. It not only contributes to the academic field by shedding light on various sports betting strategies and their effectiveness but also serves as a foundational element for the application. This analysis will explore questions such as the optimal timing for placing hedging bets and how these opportunities vary across different sports and betting environments. Furthermore, it will examine the financial implications of these strategies, providing a clear picture of their potential profitability.

## Ethical Implications

This thesis acknowledges the significant ethical considerations inherent in sports betting. A primary concern is ensuring that the application and its recommendations do not inadvertently foster gambling addiction or encourage irresponsible betting practices. This involves a commitment to promoting responsible gambling, providing users with information that highlights safe betting habits and the potential risks associated with gambling. Compliance with legal and regulatory standards in sports betting is another crucial aspect of this research, ensuring that the project adheres to the ethical and legal frameworks governing the industry. By addressing these ethical issues, the thesis aims to make a positive contribution to the sports betting field, enhancing user experience while promoting responsible and ethical gambling practices.

To assist you in elaborating on these issues, the following areas are topics you might
consider addressing. You do not need to address all of them.

* Information Privacy
* Information Accuracy (e.g. can contain reliability)
* Potential Misuse (e.g. computer crime, unintended consequences)
* Second- or Third-Party Risk (e.g. safety)
* Data Collection Issues (e.g. issues inherent in collecting data)
* Algorithmic or Data Bias
* Potential Power Difference / Social Imbalance / Issues in Equity

In addition, reflect on ways that the above harms can be or are mitigated by your work

# Related work

This chapter includes a broad and detailed review of relevant existing work.
The literature review should provide background and context for the thesis work.
The subsections may be organized in whatever manner seems best suited to the material--
chronological, or by topic, or according to some other criteria
(e.g., primary versus secondary resources).

If ethical issues are central to this work, you should also address historical and
contemporary issues or efforts made to address them.

# Method of approach

This chapter answers the "how" question - how did you complete your project,
including the overall design of your study, details of the algorithms and tools you
have used, etc.  Use technical diagrams, equations, algorithms, and paragraphs of text
to describe the research that you have completed. Be sure to number all figures and
tables and to explicitly refer to them in your text.

This should contain:

* lists
* with points
* and more points
  * possibly subpoints

For those projects whose implications address social or moral issues (i.e. ethical
standards, causes, effects), you will want to use this section to describe how you
actively mitigated or considered these issues.

# Experiments

This chapter describes your experimental set up and evaluation. It should also
produce and describe the results of your study. The section titles below offer
a typical structure used for this chapter.

## Experimental Design

Especially as it pertains to responisble computing, if conducting experiments or
evaluations that involve particular ethical considerations, detail those issues here.

## Evaluation

## Threats to Validity

# Conclusion

Traditionally, this chapter addresses the areas proposed below as sections, although
not necessarily in this order or organized as offered. However, the last section --
"Ethical Implcations" is required for this chapter. See the heading below for more
details.

## Summary of Results

## Future Work

## Future Ethical Implications and Recommendations

Especially as pertains to the public release or use of your software or methods, what
unresolved or special issues remain? What recommendations might you make?

## Conclusions


# References

::: {#refs}
:::
