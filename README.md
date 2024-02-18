# Z2M-ember-devlogs

<a href="https://www.buymeacoffee.com/Nerivec" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

Some dev stuff related to the [new ember implementation](https://github.com/Nerivec/zigbee-herdsman/tree/alt-ember) ([introducing PR](https://github.com/Koenkk/zigbee-herdsman/pull/918)) for [zigbee-herdsman](https://github.com/Koenkk/zigbee2mqtt).

Logs are abbreviated to the relevant parts...

# Backup/Restore

Number indicates time-order.

1. Forced a start of the NCP with just a network leave ("new adapter" state), then restored backup.
2. Used `GENERATE` to force forming from config (adapter/backup no match).
3. Restored backup after 2.
4. Same as 2. except removed backup file just to test code path.
5. One last restore from backup after "clean-slate" (clean form+MQTT restart just because...).

# Other

### Log excerpt

Interviews with a few different devices.

### Internal Reset

Shows the NCP reset logic in action.

### Save tokens

A couple fo runs of tokens exporting. _Removed the actual tokens, just because..._

# NCP Counters

Retrieve 5min after start (hence the low numbers); with one device offline for testing.

- MAC_RX_BROADCAST: 44
- MAC_TX_BROADCAST: 62
- MAC_RX_UNICAST: 10
- MAC_TX_UNICAST_SUCCESS: 4
- MAC_TX_UNICAST_RETRY: 0
- MAC_TX_UNICAST_FAILED: 0
- APS_DATA_RX_BROADCAST: 3
- APS_DATA_TX_BROADCAST: 3
- APS_DATA_RX_UNICAST: 4
- APS_DATA_TX_UNICAST_SUCCESS: 3
- APS_DATA_TX_UNICAST_RETRY: 0
- APS_DATA_TX_UNICAST_FAILED: 2
- ROUTE_DISCOVERY_INITIATED: 8
- NEIGHBOR_ADDED: 1
- NEIGHBOR_REMOVED: 0
- NEIGHBOR_STALE: 0
- JOIN_INDICATION: 0
- CHILD_REMOVED: 0
- ASH_OVERFLOW_ERROR: 0
- ASH_FRAMING_ERROR: 0
- ASH_OVERRUN_ERROR: 0
- NWK_FRAME_COUNTER_FAILURE: 0
- APS_FRAME_COUNTER_FAILURE: 0
- ASH_XOFF: 0
- APS_LINK_KEY_NOT_AUTHORIZED: 0
- NWK_DECRYPTION_FAILURE: 0
- APS_DECRYPTION_FAILURE: 0
- ALLOCATE_PACKET_BUFFER_FAILURE: 0
- RELAYED_UNICAST: 0
- PHY_TO_MAC_QUEUE_LIMIT_REACHED: 0
- PACKET_VALIDATE_LIBRARY_DROPPED_COUNT: 0
- TYPE_NWK_RETRY_OVERFLOW: 0
- PHY_CCA_FAIL_COUNT: 0
- BROADCAST_TABLE_FULL: 0
- PTA_LO_PRI_REQUESTED: 0
- PTA_HI_PRI_REQUESTED: 0
- PTA_LO_PRI_DENIED: 0
- PTA_HI_PRI_DENIED: 0
- PTA_LO_PRI_TX_ABORTED: 0
- PTA_HI_PRI_TX_ABORTED: 0
- ADDRESS_CONFLICT_SENT: 0
