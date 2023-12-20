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

This thesis presents a detailed study and development of an application focused on sports betting odds, with an emphasis on identifying, optimizing, and notifying users about hedging opportunities. Hedging in sports betting involves placing wagers on both outcomes of a binary betting option to ensure a profit, irrespective of the final result. Such opportunities are found when the odds are structured so that the total payout exceeds the sum wagered. These opportunities typically occur during live betting situations, where a bettor places a bet either before or during a game, and due to events during hte game the odds change dramatically enough to allow the user to ensure profit by betting on the other option. Additionally, this thesis will also conduct a historical data analysis to determine the feasibility of this strategy, and when it makes sense for the bettor to hedge.

## Motivation

The impetus behind this research stems from two principal aims. The first is to create an application where a bettor can inform the application of a bet they made on another platform, and the application will be able to mathematically determine and notify the bettor if there is a hedging opportunity available, and inform them of what they would need to bet to maximize profit. The second aim is to contribute to the body of knowledge in sports betting by conducting a historical analysis of betting odds, focusing on the profitability of hedging your bets and when a bettor should do so. This part of the research aims to provide insights into the mechanics and strategic use of hedging bets. The overarching goal is to offer a tool that not only aids bettors in making more informed decisions but also helps in curbing the adverse effects of gambling, such as addiction and financial losses.

This tool and research are necessary due to the rapidly growing size of the sports betting industry an the lack of research regarding betting strategies and tools that can be used to both increase profitability and decrease gambling addiction risk. Most of the research done thus far has been conducted in Europe which has completely different gambling laws and regulations as well as a very different sports culture than what is seen in America, so there must be more research done in the states to assess the impact and potentially positive strategies and tools that can make sport betting safer and more entertaining for United States residents. Though there are major differences, valuable insights can be taken from the research that has been done in Europe thus far. In Europe alone the gross gaming revenue of sports betting was 41.7 billion Euros in 2020, with 55% of all bets being placed during the course of a sporting event. [@MichelsOttingLangrock2023] Meanwhile, little research has been done to examine how users can maximize their odds during live betting scenarios, and the implications using a hedging strategy might have on profitability and the prevelance of problematic gambling habits.

## Current State of the Art

The landscape of sports betting research, particularly in the context of hedging strategies, is currently limited. Most of the available literature is focused on markets outside the United States, or it concentrates on predicting outcomes of sports events and identifying bets with favorable odds. This thesis distinguishes itself by not predicting outcomes or assessing odds fairness. Instead, it focuses on presenting users with profitable betting options based on current market conditions and data from the-odds-api. [@theoddsapi23] A significant aspect of this research is the historical analysis of sports betting odds, an area that has not been thoroughly explored in existing literature. This analysis extends beyond theoretical models, providing a practical examination of historical outcomes and trends in sports betting odds.

## Goals of the Project

The thesis is structured around two primary objectives. The first is a comprehensive historical analysis to ascertain the occurrence and profitability of hedging opportunities in comparison to traditional betting strategies. This involves a systematic examination of odds data from previous sporting events to identify the prevalence and profitability of hedging strategies when compared betting solely based on what you believe the outcome will be. The second objective is the development of an application that pulls in real time odds data in order to identify and notify users of hedging opportunities and how to take advantage of them.

The historical analysis portion of the thesis is critical. It not only contributes to the academic field by shedding light on various sports betting strategies and their effectiveness but also serves as a foundational element for the application. This analysis will explore questions such as the optimal timing for placing hedging bets and how often these opportunities occur and when they are a favorable option when compared to sticking with your bet. Furthermore, it will examine the financial implications of this strategy, providing a clear picture of it's potential profitability.

## Ethical Implications

This thesis acknowledges the significant ethical considerations inherent in sports betting. A primary concern is ensuring that the application and its recommendations do not inadvertently foster gambling addiction or encourage irresponsible betting practices. This involves a commitment to promoting responsible gambling, providing users with information that highlights safe betting habits and the potential risks associated with gambling. Compliance with legal and regulatory standards in sports betting is another crucial aspect of this research, ensuring that the project adheres to the ethical and legal frameworks governing the industry. By addressing these ethical issues, the thesis aims to make a positive contribution to the sports betting field, enhancing user experience while promoting responsible and ethical gambling practices.

These concerns are addressed by a few key strategies that aim to mitigate the risk of gambling addiction. First, the application does not allow the user to place bets using it, nor will it handle money of any kind. Also, the unique position and niche of this research should enable users to avoid or mitigate many of the traditional pitfalls of gambling. Research indicates that live betting is traditionally problematic for users, and much of the negative behavior is linked to the feeling of having input and options in real time, as well as the ability to chase your losses using the "cash out" button found on most modern sportsbooks, that allow you to settle your bets early for an amount tied to the probability of your bet winning. [@KillickAndGriffiths2020] My application takes some of this control out of your hand by taking attention away from the betting platform and the especially dangerous "cash out" button, and instead putting you in a place where you are given live accurate information on how and where you can profit. This should theoretically remove some of the emotional decision making that typically causes gamblers losses and feeds into problematic gambling tendencies.

This work and app are heavily limited by third-party risk, which can not be eliminated. Due to the lack of regulation around sports betting and the fact that the industry's progression is currently outpacing regulation it is hard to verify the accuracy of the odds data we are receiving. While conducting this research and testing my application I have manually verified the accuracy of the data I am receiving from *the-odds-api*, but this is in no way conclusive or comprehensive. Additionally, *the-odds-api* gives no information on how it is able to access all of the odds across different sportbooks, and makes no promises about the integrity or reliability of their data. [@theoddsapi23] This introduces a fundamental risk about the longevity and reliablility of the findings of this project and the long term maintainability of the application.However, throughout research and testing there have been no sings that the data is in any way inaccurate or compromised, but the risk still remains. Which means it must be acknowledged that this application can make no promises of 100 percent accuracy, and anyone who chooses to use the application should verify the accuracy of the data it provides **before** placing any wagers. Unfortunately, this is a problem inherent to the industry at this point in time. Even sportsbooks such as *DraftKings* will not offer any guarentees about the integrity of their own data and make sure to explicitly state as much in their terms of use. [@draftkings2023] This is a problem that cannot be avoided if any investigation into sportsbook odds data is conducted, thus my strategy of gathering and verifying data is as thorough as is possible at this point in time.

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
