# elementum-x-backend

Here lives the Off-chain Keepers (Bots)

### What they do?

Watch the on-chain PositionManager state.

Listen to PositionOpened, PositionModified events.

Use indexer/graph or direct node access to track active positions.

Compare mark price (from oracle) to position entry + margin to determine liquidation eligibility.

When liquidation threshold is hit, bot sends tx to:

PositionManager.liquidatePosition(positionId)
