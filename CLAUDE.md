# lexware-php-api

## Overview
PHP 8 client library for Lexware Office (formerly lexoffice) API. Enables PHP applications to integrate with German accounting software Lexware Office.

## Repository Purpose
- **Lexware integration** - Connect PHP apps to Lexware Office
- **German accounting** - Invoicing, contacts, payments
- **API client** - Wrapper for Lexware Office API
- **Business automation** - Automate accounting workflows

## Key Features

### API Coverage
- Invoices (Rechnungen)
- Contacts (Kontakte)
- Vouchers (Belege)
- Payments (Zahlungen)
- Credit notes (Gutschriften)
- Order confirmations (Auftragsbestätigungen)
- Delivery notes (Lieferscheine)
- Quotations (Angebote)

### Functionality
- Create, read, update, delete operations
- PDF generation and retrieval
- Search and filtering
- Error handling with exceptions
- Type-safe operations
- Pagination support

### Technical Details
- **PHP 8+** - Modern PHP features
- **Composer** - Package manager integration
- **PSR compliant** - Follows PHP standards
- **Exception handling** - LexwareException class
- **Well documented** - Wiki documentation

## Installation

### Via Composer
```bash
composer require baebeca/lexware-php-api:~2.0
```

### composer.json
```json
{
  "require": {
    "baebeca/lexware-php-api": "~2.0"
  }
}
```

## Basic Usage

```php
<?php
require __DIR__.'/vendor/autoload.php';
use \Baebeca\LexwareApi;
use \Baebeca\LexwareException;

$lexware = new LexwareApi([
    'api_key' => 'my-api-key'
]);

try {
    $invoices = $lexware->get_last_invoices(-5);
} catch (LexwareException $e) {
    var_dump($e->getMessage());
    print_r($e->getError());
}
```

## Use Cases
1. **Automated invoicing** - Generate invoices from PHP app
2. **E-commerce integration** - Sync orders to Lexware
3. **CRM integration** - Sync contacts and customers
4. **Financial reporting** - Extract accounting data
5. **Document automation** - Generate PDFs
6. **Business workflows** - Automate accounting tasks

## Target Audience
- German businesses using Lexware Office
- PHP developers
- E-commerce platforms
- SaaS applications
- Accounting automation tools
- German market web applications

## Provider
- **Developer**: Baebeca Solutions
- **Lexware Partner**: Official Lexware Technology Partner
- **Package**: Available on Packagist
- **License**: Commercial and free versions available

## Resources
- [GitHub Repository](https://github.com/Baebeca-Solutions/lexware-php-api)
- [Wiki Documentation](https://wiki.baebeca.de/index.php?title=lexware-php-api)
- [Project Page](https://www.baebeca.de/softwareentwicklung/lexware-php-client/)
- [Packagist](https://packagist.org/packages/baebeca/lexware-php-api)
- [Lexware Office API Documentation](https://developers.lexware.io)

## Support
- **Commercial license holders**: Ticket system
- **Free version**: Community support

## German Market Context
- **Lexware Office** - Leading German accounting SaaS
- **Compliance** - German tax and accounting standards
- **Integration** - Common in German e-commerce
- **Language**: German documentation and interface

## Related User Context
Based on user's other projects:
- User runs a German Handwerk (trade) business
- Likely uses Lexware for accounting
- Integration with Field Service Management
- Potential connection to Handwerk-AI-Agenten project

## Important Notes
- **German market** - Specifically for German accounting
- **API key required** - Lexware Office account needed
- **Commercial options** - Paid support available
- **Well maintained** - Active development
- **Lexware Partner** - Official technology partner status

## Version History
- v2.0 - PHP 8 version (current)
- Previously: lexoffice-php-api
- Migration guide available

## Migration
See README-MIGRATE-TO-COMPOSER-VERSION.md for upgrading from older versions.
