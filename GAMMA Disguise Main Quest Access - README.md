# GAMMA Disguise Main Quest Access

Version `d2026.11.16.1`

Lets a G.A.M.M.A. character take the main story lines while wearing a faction
disguise. Anomaly opens these conversations only for the faction you really
belong to, so a disguise never gets you in. This mod makes them follow the
faction you are disguised as.

## What it does

Each of these checks your faction first. This mod changes that check from your
real faction to your current one, which is the disguise when you wear one:

- the first talk about the story quest lines with Sidorovich, Petrenko, Lukash,
  Cold, Sakharov and Dushman;
- Living Legend, Mortal Sin and Operation Afterglow with Sidorovich, Voronin,
  Lukash, Cold, Sakharov and Dushman, from taking them to reporting back;
- the Sin envoy's greeting to Mercenaries in Mortal Sin;
- Urgent Orders from iTheon's New Tasks. It is not a conversation: Duty sends
  it to you about 20 seconds after you arrive in the Bar or load a save there,
  and the Army does the same in Agroprom, at most once every five days. Once you
  have it, the task remembers which of the two gave it, so changing your
  disguise does not make its messages come from the wrong leader.

It also opens Operation Afterglow for a character whose real faction has no
story line of its own, such as a Renegade or a Bandit. Anomaly announces
Afterglow by PDA news, which it sends only when your real faction is Loners,
Duty, Freedom, Clear Sky, Ecologists or Mercenaries. For anyone else this mod
opens it as soon as Mortal Sin's last talk with the leader is done, or when you
load a save made after that talk. There is no PDA message in that case. Take
Afterglow from the leader whose disguise you wear, like the other story lines,
and keep a story faction's disguise on for the whole of it: Colonel Degtyarev
and the military on Jupiter and in Pripyat treat Renegades and Bandits as
enemies, so they will not talk to you and will fight back.

Wear the disguise when you talk to the leader, and when you arrive on the level
for Urgent Orders. Any suit of another faction counts as a disguise unless its
patch has been torn off. While a disguise is on, your real faction's
conversations wait until you take it off: a Duty character disguised as Freedom
gets Lukash's story conversations and not Voronin's, and does not get Duty's
Urgent Orders.

What it deliberately leaves alone:

- Anomaly's disguise itself: when it works and when NPCs see through it.
- The other conditions on those conversations, such as story mode being off or
  a faction-limited playthrough.
- The story and quest content.

## Requirements

- S.T.A.L.K.E.R. Anomaly 1.5.3.
- GAMMA, modpack definition 920 (built and checked against it; only briefly
  tested in game, see Known issues).
- No other mod is needed.

## Installation

1. Exit the game. In MO2, use the **Install Mod** button, pick the `.7z`, name
   the mod `GAMMA Disguise Main Quest Access` and enable it.
2. It replaces five files, so it must sit **below** these four mods in MO2's
   left pane: `G.A.M.M.A. Quests Rebalance`,
   `G.A.M.M.A. Economy (don't disable, turn on Black Market to buy gear)`,
   `Anomaly 1.5.2 fixes` and `403- New Tasks - iTheon`. A newly installed mod
   goes to the bottom, so this is normally already true.

## Compatibility and conflicts

- It ships whole copies of `dialogs.xml`, `dialogs_lostzone_ll.xml`,
  `dialogs_lostzone_ms.xml`, `dialogs_lostzone_oa.xml` and
  `tasks_urgent_orders.script`, each GAMMA's or Anomaly's own file with only
  the changes above. It also adds one script of its own,
  `gamma_disguise_afterglow.script`, which replaces no file and only reacts to
  Anomaly's own game events. If another mod ships one of the five replaced
  files, whichever sits lower in MO2 wins and the other's changes to that file
  are lost. GAMMA's
  optional `Pre-0.9.3.1 Saves Fix` (`tasks_urgent_orders.script`) and
  `G.A.M.M.A. Companions Rework` (`dialogs.xml`), both off by default, are such
  mods.
- If a GAMMA update changes one of the five files, this mod keeps the older
  copy until it is rebuilt.
- GAMMA's development branch does not change any of the five files, according
  to a comparison of its file lists. It has not been run with this mod.

## Options

No options.

## Adding or removing mid-save

Adding it is designed to be safe. Removing it is not expected to cause errors,
but finish any story line you took through a disguise first. Afterwards only a
leader of your real faction can take your reports, the journal task from the
disguised leader stays open and its reward is lost, and a character whose real
faction has no story leader (Army, Bandit, Renegade, Monolith, Sin) cannot
report at all.

It keeps one extra value in Urgent Orders' own save data, which the original
script ignores. An Urgent Orders task taken before you added the mod picks who
sends its messages from your current disguise. Neither adding nor removing has
been tested in game.

A character whose real faction has no story line and who finished Mortal Sin
with an earlier version of this mod gets Operation Afterglow as soon as this
version is installed and the save is loaded. Removing the mod leaves that flag
in the save, but without the mod no leader offers Afterglow to such a
character, so take it and finish it before removing the mod.

## Uninstall

Disable or remove the mod in MO2, after reading the section above. Saves keep
the one extra Urgent Orders value, which the original script ignores, and the
Operation Afterglow flag described above. Nothing else is left behind.

## Known issues

- The five replaced files, unchanged since the previous release, have had four
  short scripted runs in game, each on one save, with no errors from this mod in
  the log. In the last two, a real Loner put on a Clear Sky suit where nobody
  saw it, the game's own disguise took effect, and, with the test script placing
  him beside Cold, Cold offered the first talk about the story quest lines,
  which he had not offered before. Choosing it gave Cold's briefing, and Living
  Legend's first topic appeared. In another run, with the faction switched by
  script, the story conditions and Urgent Orders' choice of leader followed it.
  No story line was played through and no Urgent Orders task was given in game.
  The four dialogue files carry the same changes as the copy the author has had
  installed since July 2026.
- Stay with one leader for a whole story line. The leaders' report conversations
  check only your current faction and your progress, not who gave you the line,
  so changing or removing the disguise can show another leader's report. At the
  end of Living Legend that report moves the story on, but the first leader's
  journal task and reward stay open until you go back to them in their disguise.
  In Mortal Sin it moves the next step to the new leader, while later steps
  still point at the first one.
- Monolith and Sin characters cannot start Mortal Sin, because a new game
  marks it as already started for them; Anomaly decides that outside these
  conversations.
- A character whose real faction has no story line gets no PDA message when
  Operation Afterglow opens, nor the later PDA tip that points to Degtyarev on
  Jupiter. Nothing in the story depends on either message.
- The Afterglow change has only been tested against stand-ins for the game,
  not in game.

## Changelog

### d2026.11.16.1

- Operation Afterglow now opens for characters whose real faction has no story
  line, such as Renegades, once Mortal Sin's last talk with the leader is done.
  Anomaly opens it only for Loners, Duty, Freedom, Clear Sky, Ecologists and
  Mercenaries. Saves that already finished Mortal Sin get it when loaded.

### d2026.11.9.1

- First public release.

## Credits

- The S.T.A.L.K.E.R. Anomaly team, for the story dialogues and the disguise
  system.
- DoctorX, for the Questlines dialogues.
- Grokitach and the G.A.M.M.A. contributors, for the versions of these files
  that GAMMA ships.
- iTheon, for New Tasks and its Urgent Orders script.

## Licence

CC BY-NC-SA 4.0 for the author's changes; see
`GAMMA Disguise Main Quest Access - LICENSE.txt`.
