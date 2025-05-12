# Browser fingerprinting demo

```
// Browser fingerprint collector
function generateFingerprint() {
    const canvas = document.createElement('canvas');
    const gl = canvas.getContext('webgl') || canvas.getContext('experimental-webgl');
    
    return {
        userAgent: navigator.userAgent,
        screenResolution: `${window.screen.width}x${window.screen.height}`,
        timezone: new Date().getTimezoneOffset(),
        cookiesEnabled: navigator.cookieEnabled,
        hardwareConcurrency: navigator.hardwareConcurrency || 'unknown',
        webglVendor: gl ? gl.getParameter(gl.VENDOR) : 'none',
        webglRenderer: gl ? gl.getParameter(gl.RENDERER) : 'none',
        fonts: getFontList()
    };
}

function getFontList() {
    const fonts = [
        'Arial', 'Times New Roman', 'Courier New', 
        'Comic Sans MS', 'Verdana', 'Georgia'
    ];
    return fonts.filter(font => {
        const span = document.createElement('span');
        span.style.fontFamily = font;
        span.style.position = 'absolute';
        span.style.left = '-9999px';
        span.innerHTML = 'abcdefghijklmnopqrstuvwxyz';
        document.body.appendChild(span);
        const width = span.offsetWidth;
        document.body.removeChild(span);
        return width !== document.createElement('span').offsetWidth;
    });
}
```

