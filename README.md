# AI Migration Project

AI conversation context and memory management system. Organizes and migrates AI interaction data across sessions and platforms.

## Structure

```
├── active_context/          # Current active conversation context
├── conversations/           # Stored conversation data and embeddings
│   ├── omni_conversations_vector_embedding/
│   ├── symbol_tags_organized.json
│   └── ...
├── convert_symbolic_field_Analyzer/  # Field analysis tools
├── memory/                  # Memory management
└── transcripts/             # Conversation transcripts
```

## Components

- **Vector embeddings** — conversation data indexed for semantic search
- **Symbol tagging** — organized by symbolic field analysis
- **Memory management** — persistent cross-session context
- **Transcript processing** — import/export conversation logs
