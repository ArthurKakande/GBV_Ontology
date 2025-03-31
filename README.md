# Africa Gender-Based Violence Lexicon Ontology

Welcome to the **Africa Gender-Based Violence Lexicon Ontology** repository! This ontology provides a structured and comprehensive framework for understanding and analyzing terms, concepts, support organsiations and legal frameworks related to gender-based violence (GBV). It is designed to support researchers, policymakers, activists, and developers in building knowledge graphs, applications, and tools to address GBV (or TFGBV).

The preferred prefix for this ontology is **ogbv: www.gbvbase.com**

## Overview

This ontology captures:
- **GBV-related terms** (e.g., "malaya", "prostitute" "slut-shaming") and their meanings.
- **Forms of violence** (e.g., psychological, verbal, physical).
- **Implications** of GBV (e.g., emotional trauma, social stigma).
- **Targeted gender(s)** (e.g., women, men).
- **Geographical context** (e.g., countries, regions, continents).
- **Legal frameworks and policies** addressing GBV (e.g., laws, enforcement agencies, effectiveness ratings).

The ontology is built using **OWL (Web Ontology Language)** and is designed to be extensible, modular, and interoperable with other knowledge graphs and semantic web tools.

---

## Key Features

- **Comprehensive Coverage**: Captures terms, meanings, implications, and legal frameworks related to GBV.
- **Geographical Context**: Includes countries, regions, and continents, with a focus on Africa.
- **Legal Frameworks**: Tracks laws, policies, enforcement agencies, and effectiveness ratings.
- **Modular Design**: Easy to extend with new terms, regions, or legal provisions.
- **Publicly Accessible**: Free to use and adapt under an open-source license.

---

## Ontology Structure

### Classes
- **Word**: Terms related to GBV (e.g., "malaya", "slut-shaming").
- **Meaning**: Definitions of terms.
- **FormOfViolence**: Types of violence (e.g., psychological, verbal).
- **Implication**: Consequences of GBV (e.g., emotional trauma).
- **GenderTargeted**: Genders affected by GBV (e.g., women, men).
- **Continent**, **Region**, **Country**: Geographical context.
- **LegalFramework**, **Policy**, **LegalProvision**: Laws and policies addressing GBV.
- **EnforcementAgency**: Organizations responsible for enforcing laws.
- **EffectivenessRating**: Evaluations of legal frameworks and policies.

### Properties
- **Object Properties**: Relationships between classes (e.g., `hasLegalFramework`, `targetsGender`).
- **Data Properties**: Attributes of classes (e.g., `wordText`, `yearEnacted`).

---

## How to Use

### Access the Ontology
The ontology is available in **OWL format** and can be downloaded from the [Releases](https://github.com/pollicy/GBVOntology) section.

### Explore the Ontology
- Use tools like **[Protégé](https://protege.stanford.edu/)** or **[WebVOWL](https://service.tib.eu/webvowl/)** to visualize and explore the ontology.
- Load the ontology into a **triplestore** (e.g., Apache Jena, Stardog) for querying and integration with other datasets.

### Extend the Ontology
- Add new terms, regions, or legal frameworks by extending the existing classes and properties.
- Contribute to the ontology by submitting a pull request.

---

## Example Queries

Here are some example SPARQL queries to get started:

1. **Find all GBV-related terms used in Nigeria:**
    ```sparql
    SELECT ?word ?meaning
    WHERE {
         ?word a :Word ;
                 :hasMeaning ?meaning ;
                 :usedInCountry :Nigeria .
    }
    ```

2. **List all legal frameworks in Africa with their effectiveness ratings:**
    ```sparql
    SELECT ?framework ?rating
    WHERE {
         ?framework a :LegalFramework ;
                        :hasEffectivenessRating ?rating ;
                        :hasLegalFramework ?country .
         ?country :locatedInContinent :Africa .
    }
    ```
    ## Contributing

    We welcome contributions to improve and expand this ontology! Here’s how you can help:

    - **Report issues**: Found a bug or have a suggestion? Open an issue.
    - **Submit pull requests**: Add new terms, regions, or legal frameworks.
    - **Share feedback**: Let us know how you’re using the ontology and how we can make it better.

    Please read our [Contribution Guidelines](CONTRIBUTING.md) for more details.

    ## License

    This ontology is released under the MIT License, making it free to use, modify, and distribute. If you use this ontology in your work, please cite this repository.

    ## Cite This Work

    If you use this ontology in your research or projects, please cite it as follows:

    ```
    Kakande, A. (2025). Gender-Based Violence Lexicon Ontology. Retrieved from https://github.com/pollicy/GBVOntology
    ```
    You can also cite it using the following BibTeX entry for LaTeX:

    ```bibtex
    @misc{kakande2025gender,
        author = {Arthur Kakande},
        title = {Gender-Based Violence Lexicon Ontology},
        year = {2025},
        howpublished = {\url{https://github.com/pollicy/GBVOntology}},
    }
    ```

    For questions, collaborations, or feedback, please reach out to:

    - **Project Maintainer**:  [Arthur Kakande](https://www.linkedin.com/in/arthur-kakande-9b2870b9/)

    Thank you for using the Gender-Based Violence Lexicon Ontology! Together, we can build tools and knowledge to combat gender-based violence and create a safer world for all.
