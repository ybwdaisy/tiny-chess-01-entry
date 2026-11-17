# tiny-chess-01 entry

A chess engine in at most 4,096 bytes of Python (main.py), built for the
make.fun tiny-chess-01 bounty. Negamax search with alpha-beta pruning,
quiescence, a transposition table and piece-square evaluation; it plays
to a fixed node budget, never a clock, so trials replay move for move.

Run by the harness as `python3 -P -s /bot/main.py`; it talks only to the
env at MAKEFUN_ENV_URL.
