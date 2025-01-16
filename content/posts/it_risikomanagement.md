---
title: "IT-Risikomanagement"
date: 2025-01-15T22:31:41+02:00
draft: false
tags: ["risikomanagement"]
ShowToc: true
---

Risikomanagement ist in vielen Bereichen wichtig, darunter auch in der IT. Während man es oft mit dem System Engineering und OPS verbindet, kann auch in der Softwareentwicklung ein effektiver Risikomanagementprozess implementiert werden – allerdings mit einem anderen Schwerpunkt.  In manchen Branchen ist IT-Risikomanagement gesetzlich oder durch externe Stellen verpflichtend. Oft gibt es jedoch keine konkreten Vorgaben, wie ein solcher Prozess aussehen muss, sondern lediglich die Anforderung, dass ein Prozess vorhanden sein sollte. Bei bestimmten Zertifizierungen, wie etwa **ISO 27001**, **NIST**, oder **Basel III**, wird ein Risikomanagementprozess ebenfalls vorausgesetzt. Doch auch ohne gesetzliche Verpflichtung ist es für Organisationen sinnvoll, ein Risikomanagementsystem einzuführen, da es langfristig mehr Transparenz und Sicherheit schafft.

## Risikomanagement-Prozess
Im Kern geht es darum, potenzielle Ereignisse zu analysieren, die die IT-Infrastruktur beeinflussen könnten, deren Auswirkungen zu bewerten und geeignete Maßnahmen zu ergreifen. Dieser Prozess hilft, Schwachstellen zu identifizieren, Auswirkungen zu verstehen und den Aufwand für Gegenmaßnahmen zu priorisieren. Ein Risikomanagementprozess soll nicht alle Risiken beseitigen, sondern eine systematische Identifikation und Bewertung ermöglichen, um entsprechende Maßnahmen zu ergreifen.

Es gibt viele Frameworks, die als Grundlage dienen können. Zu den bekanntesten gehören sicherlich:  
- **COBIT**  
- **NIST Risk Management Framework (RMF)**  
- **ISO 31000**  

Diese Standards sind hilfreich, können aber für kleinere Organisationen oft zu komplex sein. Wichtig ist es, einen einfachen, praxisnahen Ansatz zu finden. Grundsätzlich folgt das Risikomanagement immer diesen vier  Phasen:  
1. **Risiken identifizieren**  
2. **Risiken bewerten**  
3. **Maßnahmen ergreifen**  
4. **Kontrollieren**  

### Risiken identifizieren  
Das Identifizieren von Risiken sollte nach Möglichkeit immer ein kreativer Prozess sein, bei dem Out-of-the-Box gedacht wird. Es spielt dabei keine Rolle, wie wahrscheinlich oder gravierend ein Risiko sein kann. Jedes potenzielle Risiko sollte in diesem Schritt gesammelt werden. Hierbei ist jedoch zu erwähnen, dass der Begriff Risiko nicht mehr durchgängig negativ behaftet ist. Ein Risiko kann auch eine Möglichkeit sein, etwas Positives zu erreichen oder ungeahnte Chancen zu eröffnen. Dabei sind Risiken aber immer ein Teil des Handelns. Wer keine Risiken eingehen möchte, der darf auch nichts machen.

Bei kleineren Teams empfiehlt sich ein gemeinsames Brainstorming, bei dem Ideen gesammelt werden. Je nach Organisation kann es auch hilfreich sein, Stakeholder oder Mitglieder aus anderen Abteilungen einzuladen, sofern diese relevant sind. Einen sehr ähnlichen Ansatz kann man mit dem Brainwriting verfolgen. Hierbei schreiben die Teilnehmer einzeln oder in kleinen Gruppen die Risiken, die ihnen einfallen, auf. Anschließend wird die Liste mit anderen Teams getauscht, die diese ergänzen. Es ist ebenfalls möglich, dass die Ideen anschließend im Team gemeinsam bewertet werden. Alternativ können auch Interviews geführt werden, indem einzelne Mitarbeiter oder kleine Gruppen befragt werden. Letzteres ist relativ zeitintensiv, kann aber zu wertvollen Informationen führen.


### Risiken bewerten  
Risiken können nach verschiedenen Faktoren bewertet werden. Auch die Bewertung sollte im Team gemeinsam besprochen werden. Es ist hilfreich, sich hier auf die Berufserfahrung der Mitarbeiter zu beziehen. Durch die Bewertung ergibt sich auch, ob ein Risiko für die Organisation relevant ist oder nicht. Je nach Risikoart können sich diese unterscheiden. Die wohl naheliegendsten sind Eintrittswahrscheinlichkeit und Auswirkung. Daneben gibt es aber noch weitere Faktoren:  
- **Risikoerkennung:** Wie schnell kann das Risiko erkannt werden, bevor Schaden entsteht?  
- **Kontrollierbarkeit des Risikos:** Wie gut kann das Risiko beherrscht werden?  
- **Kosten der Risikoprävention:** Welcher Aufwand muss aufgebracht werden?  
- **Risiko-Interdependenzen:** Hängt das Risiko mit anderen Risiken zusammen?  
- **Kontrollierbarkeit:** Wie gut kann das Risiko kontrolliert werden?  
- ...  

Um die Risiken zu bewerten, sollte eine Skala verwendet werden. Diese kann numerisch sein (0–10) oder simpel in niedrig, mittel und hoch unterteilt werden. Man wird häufig auf die Herausforderung stoßen, dass das Bewerten von Risiken oft schwierig oder subjektiv ist. Nehmen wir als Beispiel Day-Zero-Exploits: Wie hoch ist das Risiko, dass man davon betroffen ist? Niedrig oder hoch? Die Eintrittswahrscheinlichkeit eines Day-Zero-Exploits ist kein Risiko, das man exakt messen oder vorhersagen kann. Meist ist es schon hilfreich, wenn solche Risiken besprochen werden. Anstelle des Day-Zero-Exploits kann man sich auf dessen Auswirkung konzentrieren. Was passiert, wenn ein bestimmter Teil der Architektur betroffen ist? Welche Daten kann ein Angreifer einsehen? Welche Auswirkungen für den Geschäftsprozess hat es, wenn dieses System für mehrere Stunden oder Tage ausfällt? In der Regel wird die Bewertung der Risiken mit einer Priorisierung der Risiken abgeschlossen. Die wichtigsten Risiken benötigen dann im nächsten Schritt die meiste Aufmerksamkeit.


### Maßnahmen ergreifen  
Sobald die Risiken bewertet sind, werden Maßnahmen abgeleitet. Es gibt verschiedene Strategien welche Maßnahmen ergriffen werden können:
- **Akzeptieren:** Das Risiko wird bewusst in Kauf genommen, z. B. bei geringen Kosten oder minimaler Auswirkung.  
- **Vermeiden:** Aktivitäten, die das Risiko verursachen könnten, werden eingestellt oder verändert.  
- **Transferieren:** Das Risiko wird an Dritte, z. B. durch Versicherungen, ausgelagert.  
- **Teilen:** Das Risiko wird gemeinsam mit anderen getragen, z. B. durch Joint Ventures.  
- **Minimieren:** Maßnahmen zur Verringerung der Wahrscheinlichkeit oder der Auswirkungen des Risikos werden umgesetzt.  

Die Wahl der Strategie hängt oft von Budget, Wissen und Ressourcen ab. Unterstützung des Managements ist essenziell, um die Maßnahmen erfolgreich umzusetzen.

### Kontrollieren  
Die letzte Phase besteht darin, regelmäßig zu überprüfen, ob die Maßnahmen wirksam sind und ob neue Risiken aufgetreten sind. Ein Intervall von 6 bis 12 Monaten ist meist ausreichend. Messbare Werte (KPIs) wie die Anzahl der Sicherheitsvorfälle, Ausfallzeiten oder identifizierten Risiken helfen, die Effektivität zu bewerten. Doch oft sind qualitative Ergebnisse genauso wertvoll: Ein Risikomanagementprozess schafft ein Bewusstsein für Risiken und hilft, zukünftige Entscheidungen besser abzusichern. Dieses Wissen ist ein entscheidender Mehrwert, der oft unterschätzt wird. IT-Risikomanagement ist kein einmaliger Aufwand, sondern ein kontinuierlicher Prozess, der Organisationen hilft, Risiken zu verstehen, zu bewältigen und besser auf die Zukunft vorbereitet zu sein. Die richtige Balance zwischen Aufwand und Nutzen sowie ein klar strukturierter Ansatz sind dabei der Schlüssel zum Erfolg. Schon allein das Bewusstsein für potenzielle Risiken und deren Folgen stellt einen enormen Mehrwert dar.
