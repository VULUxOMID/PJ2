# Security Documentation

## Admin Access Security

### Overview
The admin panel has been secured with multiple layers of protection to prevent unauthorized access.

### Security Features

#### 1. **Obscure URLs**
- Old URLs: `/login.html`, `/admin.html`
- New URLs: `/secure-access.html`, `/management-portal.html`
- These URLs are not linked from the main website navigation

#### 2. **Session Management**
- **Session Timeout**: 30 minutes of inactivity
- **Auto-logout**: Automatic logout on browser close or inactivity
- **Session Validation**: Every page checks for valid session tokens
- **Secure Tokens**: Unique tokens generated for each session

#### 3. **Authentication System**
- **Username**: `admin`
- **Password**: `subjectphoto2024`
- **Lockout Protection**: 5 failed attempts = 15-minute lockout
- **Rate Limiting**: Prevents brute force attacks

#### 4. **Search Engine Protection**
- **robots.txt**: Blocks search engines from indexing admin pages
- **Meta Tags**: `noindex, nofollow, noarchive` on all admin pages
- **Hidden from Navigation**: Admin links removed from all public pages

#### 5. **Client-Side Security**
- **Input Validation**: All form inputs are validated and sanitized
- **XSS Protection**: HTML characters are escaped
- **CSRF Protection**: Session-based token validation

### Access Instructions

#### For Administrators:
1. **Direct Access**: Navigate directly to `/secure-access.html`
2. **Login**: Use the provided credentials
3. **Session Management**: Monitor the session timer in the top-right
4. **Logout**: Use the logout button or wait for auto-logout

#### For Developers:
1. **Change Default Credentials**: Edit the `ADMIN_CREDENTIALS` object in `secure-access.html`
2. **Customize Timeouts**: Modify `SESSION_TIMEOUT` and `LOCKOUT_TIME` constants
3. **Add IP Restrictions**: Implement server-side IP whitelisting for production

### Security Recommendations

#### For Production:
1. **Change Default Password**: Immediately change the default credentials
2. **HTTPS Only**: Ensure all admin pages are served over HTTPS
3. **Server-Side Validation**: Implement server-side authentication
4. **Database Storage**: Store credentials in a secure database
5. **Two-Factor Authentication**: Add 2FA for additional security
6. **Activity Logging**: Implement comprehensive access logging
7. **Regular Backups**: Backup admin data regularly

#### For Development:
1. **Local Testing**: Test all security features locally
2. **Credential Management**: Use environment variables for credentials
3. **Version Control**: Don't commit real credentials to version control

### File Structure

```
/
├── secure-access.html          # New secure login page
├── management-portal.html      # New admin dashboard
├── admin.html                  # Legacy admin (redirects to secure)
├── login.html                  # Legacy login (redirects to secure)
├── robots.txt                  # Search engine protection
└── SECURITY.md                 # This documentation
```

### Emergency Access

If you lose access to the admin panel:
1. **Check Session**: Clear browser localStorage
2. **Reset Credentials**: Edit `secure-access.html` to reset password
3. **Contact Support**: If using hosting provider, contact their support

### Security Checklist

- [x] Obscure admin URLs
- [x] Remove admin links from navigation
- [x] Implement session management
- [x] Add login attempt limiting
- [x] Block search engine indexing
- [x] Add input validation
- [x] Implement auto-logout
- [x] Create security documentation

### Future Enhancements

- [ ] Server-side authentication
- [ ] Two-factor authentication
- [ ] IP whitelisting
- [ ] Activity logging
- [ ] Password reset functionality
- [ ] Multiple admin users
- [ ] Role-based permissions

---

**Note**: This is a client-side only implementation. For production use, implement proper server-side security measures. 