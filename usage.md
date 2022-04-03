# Just copy the .obsidian folder

To use the template, just copy the `.obsidian` folder into a new
or existing Git project.

Obsidian "sees" all files at the same level as the `.obsidian`
folder and all files below that level. For instance, to let
Obsidian see all markdown files in the entire repository,
`.obsidian` should be at the same level as `.git`.

# Do not clone as a Git submodule

Just copy the `.obsidian` folder. **Do not** clone this (as a
submodule) into another project.

Why not? Obsidian writes session information to the JSON files in
the `.obsidian` folder. Think of the template as a *starting
point* and expect the JSON files in the `.obsidian` folder to
change as the project evolves.

For example, the `.obsidian/workspace` JSON file ends with a list
of `lastOpenFiles`. Obviously that list is project-specific.

Another example is the **graph view** settings in the
`.obsidian/graph.json` file. The graph view changes over time
with the project. When I diff to compare commits, changes to the
`colorGroups` query terms in `graph.json` are a clue to what I
was thinking about. Tracking `graph.json` under the project's
version control means I can replay the history of the graph
(looking at a snapshot of the graph at each commit).

