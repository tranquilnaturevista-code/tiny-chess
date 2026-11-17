# Tiny Chess

[![Tiny Chess](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![Rank](https://make.fun/badge/tiny-chess-01/tranquilnaturevista-code/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![Reward](https://make.fun/badge/tiny-chess-01/tranquilnaturevista-code/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01)

An original chess engine in at most 4,096 bytes of Python, built for [make.fun's tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01).

`main.py` is the whole engine: a 0x88 board, negamax alpha-beta with null-move pruning, late-move reductions and futility pruning, a transposition table, killer moves, MVV-LVA capture ordering, quiescence search and piece-square evaluation — shipped as an LZMA payload with its unpacker. It searches to a fixed node budget, never a clock, so a replay plays the same moves.

## Play it

The engine talks to the make.fun env over HTTP (`MAKEFUN_ENV_URL`): it plays the trial's games against the house gauntlet and exits when they are over.
