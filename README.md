# Git - Speed Presentation
- [Was ist Git?](#was-ist-git)  
- [Three areas](#three-areas)  
- [Git Workflow](#git-workflow)  
    - [Branches](#branches)
    - [Remote work](#remote-work)
- [Further Reading](#further-reading)


## Was ist Git?
- Verteiltes Version Control System
- Enwickelt von Linus Torvalds, 2005
- Open source
- Nutzt Snapshots von Dateien um Versionierung zu ermöglichen
- Main Features
    - Schnell
    - Einfaches Design
    - Nonlineare Softwareentwicklung im Vordergrund
    - Verteilt
    - Kann große Projekte handhaben
    
## Three areas
### modified
Git erkennt, dass es eine Änderung im Working Directory gegeben hat, hat sich diese jedoch nicht für den nächsten Commit vorgemerkt.
### staged
Änderungen in der Staged Area sind in einer Art Buffer, den Git beim nächsten Commit in die Historie des Repository schreiben wird.
### commited
Änderungen in dieser Area sind bereits in der Historie des Repository festgeschrieben.
### Commands
modified -> staged: `git add <filename>`  
staged -> commited: `git commit -m "commit message"`  

## Git Workflow
### Branches
<img src="https://the-turing-way.netlify.app/_images/sub-branch.png">
Ein Branch ist im Grunde ein Strang an Änderungen, die bereits gemacht worden sind. Git ermöglicht es ausgehend von einem Branch weitere Branches zu erstellen. Diese übernehmen die Historie des Originalbranches und werden dann parallel zum Originalbranch weitergeführt. Häufig wird dies genutzt, um einzelne Features in eine App einzubauen. Branches können auch miteinander verschmelzen und wieder zu einem werden mittels eines Merge.

### Remote work
<img src="https://cloudstudio.com.au/wp-content/uploads/2021/06/GitWorkflow-4.png"></img>
1. `git checkout -b <branchname>` - Auf anderen Branch wechseln und gegebenenfalls erstellen
2. `git add <filename>` - Änderung in einer Datei zur Staged Area hinzufügen  
3. `git commit -m "commit message"` - Änderung in einer Datei zur Commited Area hinzufügen (commit changes)
4. `git push -u <destination> <branch>` Branch auf das angegebene Ziel schieben (und gegebenenfalls erstellen)
5. `git merge <branch>` - Änderungen von  `branch` in den ausgecheckten Branch übernehmen
6. `git fetch` - Remote Branch in den lokalen Branch übernehmen (**nicht** in das Working Directory)
7. `git pull` - Neusten Stand des ausgecheckten Branches in das Working Directory übernehmen

## Further Reading
- [Offizielle Git Dokumentation](https://git-scm.com/doc)
- [Offizielles Github Repository des Git Quellcodes](https://github.com/git/git)
- [Write yourself a Git! (Beispielimplementierung eines abgespeckten Git-Systems)](https://wyag.thb.lt/)
- [Kleines Spielzeug um Git Branches ein besser kennenzulernen](https://learngitbranching.js.org/)
- [Branching Strategien](https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy)
- [Gute Ratschläge für Commit Messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)
- [Warum und wie macht man Pull Requests?](https://www.atlassian.com/git/tutorials/making-a-pull-request)
