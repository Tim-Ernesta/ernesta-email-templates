Every email ends with this footer, the last row of the wrapper table. It is byte-identical in all four coded templates; copy `email-code/blocks/footer.html` verbatim and never edit or remove parts of it.

Contents, top to bottom on `#262933` with `#f8f6f3` text:
1. Help line with the support icon: "Need help? Reach out to our design team: design@ernesta.com" (mailto link, bold address).
2. Four serif links (Georgia 18px / 600) separated by hairlines: Order a sample box (/pages/sample-box), Browse featured rugs (/collections/featured), Visit a showroom (/pages/showrooms), Join our Trade Program (/pages/trade-program), all on https://www.ernestarugs.com.
3. Social icons: Instagram, Facebook, YouTube.
4. "We'd love to see your projects on Instagram #ernestaathome".
5. Ernesta wordmark (`images/logo-footer.png`, 85px wide) and the address, 322 8th Ave, New York, NY, 10001.
6. Legal row: Help, Privacy Policy, Unsubscribe. Unsubscribe uses the merge tag `{{ unsubscribe_url }}`, which the ESP must resolve. The unsubscribe link is mandatory.

Images the footer needs (host them and update the `images/` paths): icon-help.png, line-footer.png, social-1.png, social-2.png, social-3.png, logo-footer.png.

Mobile behaviour comes from the shared classes in `email-code/shell.html` (`m-small`, `m-h4`, `m-padv`, `dsk`, `m-show`): vertical padding drops from 51px to 32px and text steps down a size.

Figma equivalent: Footer (dark, large and small).
