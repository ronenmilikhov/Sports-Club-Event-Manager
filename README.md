# Sports Club & Event Management System (C)

A Windows console application written in C for managing sportsmen, clubs, and event participation. The program loads its initial data from text files, provides an interactive menu, and writes changes back to the data files when the session ends.

## Requirements

- Windows
- Microsoft Visual C (`cl`), or another compiler that supports the Microsoft-specific functions used by the source, such as `_stricmp` and `_strdup`
- `SportsmanData.txt` and `EventData.txt` in the program's working directory

## Menu Operations

The interactive menu supports:

1. Add a sportsman
2. Add an event for a sportsman
3. Print a sportsman's events by last name
4. Count sportsmen who participated in an event during a year
5. Find the club with the most recorded event participations
6. Find sportsmen who participated in all of the selected sportsman's events
7. Print a club's distinct events, sorted by year
8. Delete an event by name and year for all sportsmen
9. Compare events from two clubs and create `Club.txt`

Choose `0` to end the program. Newly added sportsmen and events are saved when the program exits. The source currently does not persist all operations in the same way; for example, club creation opens `Club.txt` but does not write event records to it.

## Input File Formats

`SportsmanData.txt` uses semicolon-separated records:

```text
format:sportsman_id;first_name;last_name;club_name;gender
id;first_name;last_name;club_name;gender
```

`EventData.txt` uses comma-separated records:

```text
format:sportsman_id,event_name,location,year
sportsman_id,event_name,location,year
```

Gender values are `0` for male and `1` for female. Interactive event years must be between `2000` and `2023`.

## Implementation Notes

- Uses structs and dynamically allocated arrays for sportsmen and their events.
- Uses text-file loading and saving for sportsman and event records.
- Uses linear searches for IDs, names, clubs, and events.
- Uses the standard library `qsort` to order club events by year.
- The implementation uses Microsoft C runtime functions and is therefore not fully portable C99/C11.
- Input parsing and cleanup still have limitations; this README describes the current implementation rather than claiming complete memory-safety or leak-free behavior.

---
