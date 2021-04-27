[//]: # (title: Qodana)

[![official project](https://jb.gg/badges/official-flat-square.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)  
![](eap-alert.png)
![](banner-main.png)

**Qodana** is a code quality monitoring platform that allows companies to evaluate on multiple levels the quality of code they own, contract, or purchase.
It brings into your CI/CD pipelines all the smart features you love in the JetBrains IDEs plus adds project-level checks like clone detection and license audit.
Qodana takes different shapes: [Docker for any CI](docker-readme.md), [GitHub actions & application](github-overview.md), a [TeamCity plugin](teamcity-plugin-overview.md), and a separate [cloud service](service.md). They all share a common goal: ensuring that companies have more robust, more maintainable, and healthier code.

Qodana already supports PHP, Java, and Kotlin projects, and will eventually support all [languages and technologies](supported-technologies.md) covered by JetBrains IDEs.

## Analyse project locally

To start, pull the image from Docker Hub (only necessary to get the latest version):

```shell
docker pull jetbrains/qodana
```

and run the analysis locally:

```shell
docker run --rm -it -v <source-directory>/:/data/project/ -p 8080:8080 jetbrains/qodana --show-report
```

where `source-directory` should point to the root of your project.

Check the results in your browser at [`http://localhost:8080`](http://localhost:8080).

Please read our [Docker guide](docker-readme.md) for more options and details related to the Qodana execution.

## Run at GitHub

You can set up a workflow in your GitHub repository using the [GitHub action](github-overview.md) we published.

## License

By using Qodana, you agree to the [JetBrains EAP user agreement](https://www.jetbrains.com/legal/agreements/user_eap.html) and [JetBrains privacy policy](https://www.jetbrains.com/company/privacy.html).

## Contact

Contact us at [qodana-support@jetbrains.com](mailto:qodana-support@jetbrains.com) or via [our issue tracker](https://youtrack.jetbrains.com/newIssue?project=QD). We are eager to receive your feedback on the existing Qodana functionality and learn what other features you miss in it.
