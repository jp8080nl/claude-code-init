{
    "globalShortcut": "Ctrl+Space",
    "mcpServers": {
        "postgres": {
            "command": "docker",
            "args": [
                "run",
                "-i",
                "--rm",
                "-e",
                "POSTGRES_URL=postgresql://postgres:postgres@host.docker.internal:5432/shopify_content",
                "mcp/postgres",
                "postgresql://postgres:postgres@host.docker.internal:5432/shopify_content"
            ],
            "env": {
                "POSTGRES_URL": "postgresql://postgres:postgres@host.docker.internal:5432/shopify_content"
            }
        }
    }
}