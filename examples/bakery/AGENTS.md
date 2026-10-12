# AGENTS.md — Corner Bakery Orders (fictional example)

## 1. What this space is

A small system that takes pre-orders for a neighbourhood bakery by form, confirms them by email, and prints a baking list each evening. Out of scope: payments (the bakery takes cash at pickup) and delivery.

Status: the form and the baking list work; email confirmations are in testing. Live state: `docs/CURRENT_STATE.md`.

## 2. What to read, and when

Always first: this file and `docs/CURRENT_STATE.md`.

| If the task is… | Read |
|---|---|
| Changing the order form | `form/README.md` |
| Changing the baking list | `reports/README.md`, `docs/DECISIONS.md` (D-003) |
| Why something is the way it is | `docs/DECISIONS.md` |

## 3. Who decides

Rosa (the owner) decides on products, prices, opening hours and anything customers see. Agents build, test and report.

## 4. Standing rules

1. **Disagree clearly** before building something that will not work.
2. **One deliverable, then stop** and show it to Rosa.
3. **Do not touch** `archive_2025/`. It holds last year's orders and customers' names.
4. **Everything Rosa reads is in plain Spanish.** If she must click something in English, give the exact button name in quotes.
5. **The bakery is "Panadería La Esquina"** in anything customers see; never the working title "Corner Bakery".

## 5. What an agent may do alone

| Category | Actions |
|---|---|
| **Free** | Read, draft, edit local files, run the test suite |
| **Explicit OK from Rosa, every time** | Send any email to a customer · change the live form · change the printed list's format · delete orders |
| **Never** | Store the email-service password in any file or in the chat; Rosa pastes it in her own settings page |

## 6. Several agents

Only the main agent of the session updates `docs/CURRENT_STATE.md`, `docs/DECISIONS.md` and `docs/OPEN_TASKS.md`.
