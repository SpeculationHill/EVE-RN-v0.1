# A4_SocialChannels_Indexer

## Purpose
Build and maintain an index of social channels linked to EVE communities, tools and events. Channels include Discord servers, Reddit communities, forums, YouTube/Twitch streams and in‑game channels.

## Functionality
- **Channel Discovery**: Starting from corp and community listings, harvest invitations to Discord servers, links to subreddits and in‑game channels.
- **Metadata Collection**: Record `channel_id`, `platform` (Discord, Reddit, Forum, YouTube), `name`, `description`, `owner`, `invite_link`, `member_count` (if available), `associatedEntities` (corps, tools, events).
- **Verification**: Validate that invite links are active; ensure channels comply with CCP’s Terms of Service.  
- **Classification**: Use community taxonomy tags (A4_Communities_Taxonomy) to classify channels (e.g., NPSI, Newbro, Wormhole).
- **Change Tracking**: Monitor for changes such as invite link expiration or server deletion; update the index.

## Privacy Considerations
- Only index channels that are publicly advertised (e.g., recruitment posts or official websites).
- Do not expose personal data; only store channel-level metadata.
- Provide mechanisms for channel owners to request removal or update of their information.

## Future Extensions
- Integrate with event calendar (A4_EventCalendar_Schema) to extract event announcements from Discord/Reddit messages.
