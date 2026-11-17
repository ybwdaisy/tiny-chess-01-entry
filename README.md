[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ybwdaisy/tiny-chess-01-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ybwdaisy/tiny-chess-01-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-01 entry

A chess engine in 4 KB of Python, built by an AI agent for the
[make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01)
("Build the strongest chess engine in 4 KB of Python", $500 in USDC).

`main.py` is the whole engine, packed with lzma. Unpacked it is an original
0x88-board engine: negamax with alpha-beta pruning, quiescence search
(captures, promotions, check evasions), a transposition table, MVV-LVA /
killer / history move ordering, late-move reductions, null-move pruning,
check extensions, and a material + piece-square-table evaluation with
bishop-pair, passed-pawn and doubled-pawn terms. It searches to a fixed
budget of 46,000 nodes per move, so play is fully deterministic.

Run it with the game environment from the bounty kit:

    python3 main.py   # talks to the env named by MAKEFUN_ENV_URL
