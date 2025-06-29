# Lessons learned from other projects
The user can copy and paste these into CLUADE.md after running the /init command

- **Docker Dependencies**: When we make changes to dependencies or configuration files, we need to rebuild the Docker container to pick up those changes, not just restart it.
- **Foundation Testing**: Comprehensive testing of Phase 1 infrastructure (Redis, queues, APIs) ensures a solid foundation for future development and catches regressions early.
- **Test-Driven Development**: Running `npm install` inside containers may be needed after adding test dependencies to ensure proper installation.