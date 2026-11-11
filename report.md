# Writing a reply as Gordon Ramsay with Silvertongue's MCP server

Run: 11 Nov 2026, about 19:40 WIB (12:40 UTC). One real draft, written with a voice fetched live from Silvertongue's MCP server.

- **App, version, model:** Muse (Meta AI), model Muse Spark 1.3. Silvertongue's MCP server was connected by URL (`https://mcp.silvertongue.dev/mcp?ref=frantic-mcp-1&receipt=1`) over Streamable HTTP with a minimal client (`muse-mcp-minimal` 1.0, Python stdlib + curl). Silvertongue server version 0.1.5, MCP protocol 2025-03-26. Calls made, in order: `initialize`, `tools/list`, `search_voices` ("Gordon Ramsay"), then `get_voice_packet` for the voice below.
- **Voice and exactly what was asked:** Voice: Gordon Ramsay (`gordon-ramsay@sha256:75d1f9dd9d91c6507917eb4f50abd7c151658a95101391a9812be3d8849173f6`, lane celebrity). The exact ask: "Use Silvertongue to write my reply as Gordon Ramsay: I can't make it Friday — I have a work deadline, let's do next week instead." Packet settings: format reply, length short (12–40 words), platform WhatsApp, intensity full, edge clean, emoji off, spelling tidy.
- **Draft exactly as written:** Look, Friday's off. My deadline's still in the oven, nowhere near ready, and I'm not serving it half-baked. Next week instead, done properly, yes?
- **Does it sound like him, 1 to 10:** 7. The brisk rhythm is right: the "Look," opener, the short sentences, the food image carried through the whole line ("in the oven", "not serving it half-baked"), and the "yes?" tag at the end. It loses points because the clean edge strips out the swearing that makes Ramsay unmistakable at full heat, and with no signature roast line a reader could take it for any blunt British kitchen voice rather than Ramsay specifically.
- **One thing that confused me or didn't work:** My first MCP call used Python's urllib directly and hung until the 60-second read timeout (`TimeoutError: The read operation timed out`). The identical request via curl returned the JSON in about a second. I switched the client to curl and everything after that worked first try: `search_voices` returned exactly one match for Gordon Ramsay, and `get_voice_packet` returned the packet with the receipt line at the end. Nothing else failed.
- **One change I would make:** Next time I would fetch the packet with length standard instead of short, so the draft has room for a second Ramsay move (a question fired at the reader, or the turnaround) instead of carrying the whole voice on one food image.

Receipt: https://runx.ai/r/62cb8259bd6ceb8f8ba851000263782c877978181e1326fd24a3b665bd617eda

The draft is mine to send, written in Ramsay's studied technique; it is not presented as his words.
