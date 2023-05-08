---
title: Informationen zum Abhängigkeitsdiagramm
intro: 'Du kannst das Abhängigkeitsdiagramm verwenden, um alle Abhängigkeiten deines Projekts zu identifizieren. Das Abhängigkeitsdiagramm unterstützt eine Reihe beliebter Paketökosysteme.'
redirect_from:
  - /github/visualizing-repository-data-with-graphs/about-the-dependency-graph
  - /code-security/supply-chain-security/about-the-dependency-graph
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: overview
topics:
  - Dependency graph
  - Dependencies
  - Repositories
shortTitle: Abhängigkeitsdiagramm
---
<!--Marketing-LINK: From /features/security and /features/security/software-supply-chain pages "How GitHub's dependency graph is generated".-->

## Informationen zum Abhängigkeitsdiagramm

{% data reusables.dependabot.about-the-dependency-graph %}

Wenn du ein Commit mit Push an {% data variables.product.product_name %} überträgst, das eine unterstützte Manifest- oder Sperrdatei ändert oder dem Standardbranch hinzufügt, wird das Abhängigkeitsdiagramm automatisch aktualisiert.{% ifversion fpt or ghec %} Darüber hinaus wird das Diagramm aktualisiert, wenn jemand eine Änderung mithilfe von Push an das Repository einer deiner Abhängigkeiten überträgt.{% endif %} Informationen zu den unterstützten Ökosystemen und Manifestdateien findest du unter [Unterstützte Paketökosysteme](#supported-package-ecosystems) weiter unten.

{% data reusables.dependency-submission.dependency-submission-link %}

Beim Erstellen eines Pull Requests, der Änderungen an Abhängigkeiten enthält und auf den Standardbranch abzielt, verwendet {% data variables.product.prodname_dotcom %} das Abhängigkeitsdiagramm, um Abhängigkeitsüberprüfungen zum Pull Request hinzuzufügen. Diese geben an, ob die Abhängigkeiten Sicherheitsrisiken enthalten und zeigen ggf. die Version der Abhängigkeit an, in der die Sicherheitsanfälligkeit behoben wurde. Weitere Informationen findest du unter [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/about-dependency-review).

{% ifversion dependency-graph-sbom-export %}{% data reusables.dependency-graph.sbom-export %}{% endif %}

## Verfügbarkeit von Abhängigkeitsdiagrammen

{% ifversion fpt or ghec %} {% data reusables.dependency-graph.feature-availability %} Weitere Informationen findest du unter [AUTOTITLE](/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-security-and-analysis-settings-for-your-repository).

Repositoryadministrator*innen können das Abhängigkeitsdiagramm außerdem für private Repositorys einrichten. Weitere Informationen findest du unter [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/configuring-the-dependency-graph).

{% endif %}

{% data reusables.code-scanning.enterprise-enable-dependency-graph %}

{% data reusables.dependabot.dependabot-alerts-dependency-graph-enterprise %}

{% ifversion ghes %} Weitere Informationen zur Konfiguration des Abhängigkeitsdiagramms findest du unter [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/configuring-the-dependency-graph).{% endif %}

## Abhängigkeiten enthalten

Das Abhängigkeitsdiagramm enthält alle Abhängigkeiten eines Repositorys, die im Manifest und in den Sperrdateien oder deren Entsprechung für unterstützte Ökosysteme{% ifversion dependency-submission-api %} beschreiben werden, sowie alle Abhängigkeiten, die mit der Abhängigkeitsübermittlungs-API (Beta) übermittelt werden{% endif %}. Dies schließt Folgendes ein:

- Direkte Abhängigkeiten, die explizit in einer Manifest- oder Sperrdatei definiert sind, {% ifversion dependency-submission-api %} oder mithilfe der Abhängigkeitsübermittlungs-API (Beta) übermittelt wurden{% endif %}
- Indirekte Abhängigkeiten dieser direkten Abhängigkeiten, auch bekannt als transitive Abhängigkeiten oder Unterabhängigkeiten bezeichnet

Das Abhängigkeitsdiagramm identifiziert indirekte Abhängigkeiten{% ifversion fpt or ghec %} entweder explizit aus einer Sperrdatei oder durch Überprüfen der Abhängigkeiten deiner direkten Abhängigkeiten. Für eine optimale Zuverlässigkeit des Diagramms solltest du Sperrdateien (oder deren Entsprechungen) verwenden, da sie genau definieren, welche Versionen der direkten und indirekten Abhängigkeiten derzeit verwendet werden. Wenn du Sperrdateien verwendest, stelle auch sicher, dass alle Mitwirkenden des Repositorys dieselben Versionen verwenden, wodurch es dir erleichtert wird, Code{% else %} aus den Sperrdateien zu testen und zu debuggen{% endif %}.

Weitere Informationen dazu, wie {% data variables.product.product_name %} dabei hilft, die Abhängigkeiten in deiner Umgebung zu verstehen, findest du unter [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/about-supply-chain-security).

{% ifversion fpt or ghec %}

## Abhängige Objekte enthalten

Bei öffentlichen Repositorys werden nur öffentliche Repositorys im Bericht angezeigt, die von ihnen oder den von ihnen veröffentlichten Paketen abhängig sind. Für private Repositorys werden diese Informationen nicht im Bericht angezeigt.{% endif %}

## Verwenden des Abhängigkeitsdiagramms

Du kannst das Abhängigkeitsdiagramm verwenden, um folgende Aktionen auszuführen:

- Erkunden der Repositorys, von denen dein Code abhängig ist,{% ifversion fpt or ghec %}, und denen, die von ihm abhängig sind{% endif %}. Weitere Informationen findest du unter [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/exploring-the-dependencies-of-a-repository). {% ifversion ghec %}
- Anzeigen einer Zusammenfassung der in den Repositorys deiner Organisation verwendeten Abhängigkeiten in einem einzelnen Dashboard. Weitere Informationen findest du unter [AUTOTITLE](/organizations/collaborating-with-groups-in-organizations/viewing-insights-for-your-organization#viewing-organization-dependency-insights).{% endif %}
- Anzeigen und Aktualisieren von sicherheitsanfälligen Abhängigkeiten für dein Repository. Weitere Informationen findest du unter [AUTOTITLE](/code-security/dependabot/dependabot-alerts/about-dependabot-alerts).{% ifversion fpt or ghes or ghec %}
- Informationen zu sicherheitsanfälligen Abhängigkeiten in Pull Requests. Weitere Informationen findest du unter [AUTOTITLE](/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-dependency-changes-in-a-pull-request).{% endif %}

## Unterstützte Paket-Ökosysteme

Die empfohlenen Formate definieren explizit, welche Versionen für alle direkten und indirekten Abhängigkeiten verwendet werden. Wenn du diese Formate verwendest, ist dein Abhängigkeitsdiagramm genauer. Außerdem wird der aktuelle Build eingerichtet und ermöglicht es dem Abhängigkeitsdiagramm, Sicherheitsrisiken sowohl in direkten als auch indirekten Abhängigkeiten zu melden.{% ifversion fpt or ghec %} Aus einer Manifestdatei (oder deren Entsprechung) abgeleitete indirekte Abhängigkeiten werden aus den Prüfungen auf unsichere Abhängigkeiten ausgeschlossen.{% endif %}

| Paket-Manager | Languages | Empfohlene Formate | Alle unterstützten Formate |
| --- | --- | --- | ---|
{%- ifversion dependency-graph-rust-support %} | Cargo | Rust | `Cargo.lock` | `Cargo.toml`, `Cargo.lock` | {%- endif %} | Composer             | PHP           | `composer.lock` | `composer.json`, `composer.lock` | | NuGet | .NET languages (C#, F#, VB), C++  |   `.csproj`, `.vbproj`, `.nuspec`, `.vcxproj`, `.fsproj` |  `.csproj`, `.vbproj`, `.nuspec`, `.vcxproj`, `.fsproj`, `packages.config` | {%- ifversion github-actions-in-dependency-graph %} | {% data variables.product.prodname_actions %} workflows | YAML | `.yml`, `.yaml` | `.yml`, `.yaml` | {%- endif %} | Go modules | Go | `go.mod`| `go.mod`{% ifversion ghes < 3.9 or ghae < 3.9 %}, `go.sum`{% endif %} | | Maven | Java, Scala |  `pom.xml`  | `pom.xml`  | | npm | JavaScript |            `package-lock.json` | `package-lock.json`, `package.json`| | pip             | Python                    | `requirements.txt`, `pipfile.lock` | `requirements.txt`, `pipfile`, `pipfile.lock`, `setup.py` | {%- ifversion dependency-graph-dart-support %} | pub             | Dart                    | `pubspec.lock` | `pubspec.yaml`, `pubspec.lock` | {%- endif %} | Python Poetry | Python                    | `poetry.lock` | `poetry.lock`, `pyproject.toml` | | RubyGems             | Ruby           | `Gemfile.lock` | `Gemfile.lock`, `Gemfile`, `*.gemspec` | | Yarn | JavaScript | `yarn.lock` | `package.json`, `yarn.lock` |


{% note %}

**Hinweise:** 

* Wenn du deine Python-Abhängigkeiten in einer `setup.py`-Datei auflistest, können möglicherweise nicht alle Abhängigkeiten in deinem Projekt analysiert und aufgelistet werden.

{% ifversion ghes = 3.5 %}

* Unterstützung für {% data variables.product.prodname_actions %}-Workflows ist ab GitHub Enterprise Server 3.5.4 verfügbar. Das Feature ist in 3.5.0, 3.5.1, 3.5.2 und 3.5.3 nicht verfügbar. Informationen zum Ermitteln der verwendeten Version von {% data variables.product.product_name %} findest du unter [AUTOTITLE](/get-started/learning-about-github/about-versions-of-github-docs#github-enterprise-server).

{% endif %}{% ifversion github-actions-in-dependency-graph %}
* {% data variables.product.prodname_actions %}-Workflows müssen sich im `.github/workflows/`-Verzeichnis eines Repositorys befinden, um als Manifeste erkannt zu werden. Alle Aktionen oder Workflows, auf die mithilfe der Syntax `jobs[*].steps[*].uses` oder `jobs.<job_id>.uses` verwiesen wird, werden als Abhängigkeiten analysiert. Weitere Informationen findest du unter [AUTOTITLE](/actions/using-workflows/workflow-syntax-for-github-actions).

* {% data variables.product.prodname_actions %}-Workflowabhängigkeiten werden zu Informationszwecken im Abhängigkeitsdiagramm angezeigt. Dependabot-Warnungen werden für {% data variables.product.prodname_actions %}-Workflows derzeit nicht unterstützt.

{% endif %}

{% endnote %}

{% ifversion dependency-submission-api %}Du kannst die Abhängigkeitsübermittlungs-API (Beta) verwenden, um Abhängigkeiten aus dem Paket-Manager oder dem Ökosystem deiner Wahl zum Abhängigkeitsdiagramm hinzuzufügen, selbst dann, wenn sich das Ökosystem nicht in der Liste der unterstützen Ökosysteme (oben) befindet.{% endif %} {% data reusables.dependency-graph.dependency-submission-API-short %}

{% ifversion dependency-submission-api %}Du erhältst {% data variables.product.prodname_dependabot_alerts %} nur für Abhängigkeiten, die von einem der [unterstützten Ökosysteme](https://github.com/github/advisory-database#supported-ecosystems) von {% data variables.product.prodname_advisory_database %} stammen. Weitere Informationen zur Abhängigkeitsübermittlungs-API findest du unter [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/using-the-dependency-submission-api).{% endif %}
## Weiterführende Themen

- "[Abhängigkeitsdiagramm](https://en.wikipedia.org/wiki/Dependency_graph)" auf Wikipedia
- [AUTOTITLE](/code-security/supply-chain-security/understanding-your-software-supply-chain/exploring-the-dependencies-of-a-repository)
- [AUTOTITLE](/code-security/dependabot/dependabot-alerts/viewing-and-updating-dependabot-alerts)
- [AUTOTITLE](/code-security/dependabot/working-with-dependabot/troubleshooting-the-detection-of-vulnerable-dependencies)
