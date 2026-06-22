# Environment Configuration

## Development Environment

Development environment files should not be committed to the repository. Use `.env.example` as a template.

Copy this file to `.env` and update with your local settings:

```bash
cp .env.example .env
```

## Environment Variables

### API Configuration
- `NODE_ENV` - Environment (development, production, test)
- `PORT` - API server port (default: 3000)
- `API_URL` - API base URL

### Database
- `DB_HOST` - PostgreSQL hostname
- `DB_PORT` - PostgreSQL port (default: 5432)
- `DB_NAME` - Database name
- `DB_USER` - Database user
- `DB_PASSWORD` - Database password

### Authentication
- `JWT_SECRET` - Secret key for JWT signing
- `JWT_EXPIRY` - JWT token expiration time

### Services
- `REDIS_URL` - Redis connection URL
- `MQTT_BROKER` - MQTT broker URL

### Logging
- `LOG_LEVEL` - Logging level (debug, info, warn, error)

## Example Configuration

```env
NODE_ENV=development
PORT=3000
API_URL=http://localhost:3000

DB_HOST=localhost
DB_PORT=5432
DB_NAME=manufacturing_iot_hub
DB_USER=postgres
DB_PASSWORD=password

JWT_SECRET=your-secret-key-here
JWT_EXPIRY=7d

REDIS_URL=redis://localhost:6379
MQTT_BROKER=mqtt://localhost:1883

LOG_LEVEL=debug
```

## Production Considerations

Never commit sensitive information. For production deployments:

1. Use strong, randomly generated secrets
2. Store credentials in environment variables or secrets manager
3. Use HTTPS/TLS for all communications
4. Implement proper logging and monitoring
5. Use database connection pooling
6. Enable firewall rules and network security

See [Security Guidelines](SECURITY.md) for more details.
