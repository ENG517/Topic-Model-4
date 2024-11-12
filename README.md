# DITA Topic Model - Howrse Web Browser Game Documentation

This repo contains a DITA topic model (TM) related to reserving and applying an affix, covering a mare with a public covering, and maximizing a horse's BLUP in the online web browser game Howrse. 

## Authors

- Caimile Loy
- Kelly Rogers

## Project Maps

### User Scenario 1: Affixes
Tina is 34 years old and has played various online web browser games for the past five years. Last week, she created an account on Howrse and has been trying to learn the ins and outs of  the game. She notices that some horses in the game have a piece of italicized text beneath their names that hyperlinks to a separate page displaying a bunch of horses with that same piece of italicized text tagged under their names. On this page, she notices that the piece of italicized text is called an “affix.” Tina has also started a personal project on the game where she intends to breed Fjord unicorns, and she wants to find a way to label each of the horses born from this project so that their names indicate they are a part of this specific breeding project. She realizes that an affix could be the best way to do this.

### User Scenario 2: Coverings
Cody, a 57-year-old man, was introduced to Howrse by his wife, Anna, a little more than a month ago. He’s not totally enthralled by the game, but he wants to learn how to play because of how much it would mean to his wife if they were able to play together. Every now and then, Cody will hop online and start clicking around the game interface to see what all he can do. So far, he’s learned a bit of the basics, but he doesn’t play consistently enough to dive into the more advanced parts of the game. One thing that Cody does know, however, is that players (generally) aim to breed horses with the highest genetic potential and skill points possible, which means players must be mindful about which horses they choose to breed together to birth foals. Cody takes a look at his current studs and mares and, since he’s relatively new to the game, sees that his studs don’t have very high stats. He knows that, in order to advance his game, he needs to find a “good” stud’s covering offer for his mare. Since he doesn’t have any to offer up from his own studs, he decides he needs to find another player who does.

### User Scenario 3: Maximizing BLUP
Hazel, a 22-year-old college student, started playing Howrse two years ago. They’re active in Reddit forums and Discord servers about the game and have thoroughly enjoyed their time on Howrse. During those two years, their gameplay was mostly focused on advancing their equestrian center’s prestige, collecting rare coats on the game, and participating in forum discussion about the weekly promos that the game developers implement. However, recently, Hazel has decided that they want to join a competitive team on the server—a team that works to produce the highest quality horses (based on genetic potential and skill points) for a particular breed, the KWPN (Dutch Warmblood). Hazel knows that the top teams on the server usually move at a fast pace when they breed horses, and they only breed two horses together if both horses have a score of 100 BLUP, as this maximizes the genetic potential of the foal. There’s a great deal of strategy that goes into getting a horse to 100 BLUP, and Hazel really wants to learn so that they can prove they would be a good fit for the KWPN team. Although Hazel knows how to care for a horse in the game (including running rides, training, and entering competitions), they’re not sure where to start when it comes to increasing a horse’s BLUP score.

## Folders &amp; Files

- `.github`: Contains configuration files for "Github Actions".
- `assets`: Contains all assets used within the TM.
- `concepts`: Contains all concept topics.
- `references`: Contains all reference topics.
- `tasks`: Contains all task topics.
- `shared`: Contains all topic files that are shared across multiple maps.
- `out`: Contains all output folders.
- `themes`: Contains `.yaml` style configuration files.
- **Skeleton files**: All topic folders contain a single "skeleton" topic file for you to copy, whenever you need to quickly create a new file.
- `.keep` **files**: Ignore these files. They ensure that any empty folders are tracked by git. 
- `.gitignore`: This file tells git which files to ignore in the repo. You can leave this one be.

## Filenaming Conventions

- Task Topics: `t_verb_verbobject.dita`
- Concept Topics: `c_nounphrase.dita`
- Reference Topics: It varies, but something akin to `r_types_of_nounphrase.dita`
- Dita Maps: `_modelname.ditamap`

## Building Outputs with Github Actions

This repo uses Github Actions to create outputs. Refer to the following for details: 

- [.github/workflows/dita-ot-build-actions.yaml](.github/workflows/dita-ot-build-actions.yaml)
- [DITA User Docs - Using Github Actions](https://www.dita-ot.org/dev/topics/using-github-actions)
- [DITA Example YAML files](https://github.com/dita-ot/docs/blob/develop/samples/github-actions/build-using-a-project-file.yaml)

## Building Outputs Manually with the Command Line

See the DITA-OT user guide about how to generate output: [https://www.dita-ot.org/dev/topics/build-using-dita-command](https://www.dita-ot.org/dev/topics/build-using-dita-command)

### Sample DITA Commands

#### Help

To see all of the commands and parameters, use the following command:

```
dita --help
```

#### DITA options and arguments

```
-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file
```

#### Create an HTML5 site

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```

#### Create an HTML5 site with a custom CSS file

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
  -Dargs.cssroot='url/to/your/assets/folder' \
  -Dargs.css='${cssroot}/your-custom-css-file.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
```

#### Create a PDF

```
dita -f pdf -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```
