---
title: "Mach engine"
description: "Game engine & graphics toolkit for the future"
draft: false
layout: "unlimited"
rss_ignore: true
---

<style>
    .p-warning {
        text-align: center;
        padding: 0;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        background: red;
    }

    .p-section {
        display: flex;
        flex-direction: row;
        padding: 1rem;
        margin-top: 3rem;
        align-items: center;
        justify-content: center;
    }

    .p-section-highlight {
        margin-top: 4rem;
        margin-bottom: 2rem;
    }

    .p-section-right {
        margin-left: 1rem;
    }

    .p-img-left {
        height: 10rem;
        margin-left: 4.5rem;
    }

    .p-img-right {
        height: 10rem;
        margin-right: 4.5rem;
    }

    .p-img-small {
        height: 6rem;
    }

    .p-logo {
        margin-right: 3rem;
        margin-top: 2rem;
    }

    .p-logo > img {
        height: 10rem;
        width: 100%;
    }

    .p-early-stages-left {
        text-align: right;
        padding-right: 2rem;
        border-right: 1px solid gray;
        height: 12rem;
        justify-content: center;
        display: flex;
        flex-direction: column;
    }

    .p-early-stages-right {
        text-align: left;
    }

    h2 {
        text-align: left;
        margin-top: 0;
    }

    .p-section.sponsors img {
        width: 3rem;
        height: 3rem;
        margin: 0.25rem;
    }

    .choose-your-journey {
        width: 100%;
        overflow: hidden;
    }

    .navbar {
        z-index: 1;
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(0.5rem);
    }

    #content {
        margin-top: -3.3rem;
    }

    .choose-your-journey > .options {
        display: flex;
    }

    .choose-your-journey .engine,
    .choose-your-journey .core {
        flex-grow: 0; /* do not grow   - initial value: 0 */
        flex-shrink: 0; /* do not shrink - initial value: 1 */
        flex-basis: 60%; /* width/height  - initial value: auto */
        display: flex;
        flex-direction: column;
        height: 50rem;
    }

    .choose-your-journey .content > h1 {
        margin-top: 3rem;
    }

    .choose-your-journey .content > h2 {
        margin-bottom: 1rem;
    }

    .choose-your-journey .content > video {
        width: 30rem;
        padding: 1rem;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }

    .choose-your-journey .engine > .content,
    .choose-your-journey .core > .content {
        display: flex;
        flex-direction: column;
        text-align: left;
        margin-top: 2rem;
    }

    .choose-your-journey .core > .content {
        align-items: flex-end;
        position: relative;
        left: 25%;
        margin-right: 2rem;
        align-self: start;
    }

    .choose-your-journey .engine > .content {
        margin-left: 2rem;
        align-self: end;
        position: relative;
        right: 20%;
    }

    .choose-your-journey .engine {
        background: linear-gradient(180deg, #56113d 0%, #06071b 100%);
        clip-path: polygon(0 0, 100% 0, 70% 100%, 0% 100%);
    }

    .choose-your-journey .core {
        background: linear-gradient(180deg, #263fb2 0%, #06071b 100%);
        clip-path: polygon(30% 0, 100% 0, 100% 100%, 0% 100%);
        position: relative;
        left: -17%;
    }

    .community {
        background: linear-gradient(180deg, #06071b 0%, #56113d 10%, #06071b 100%);
    }

    .community > .p-section > div {
        width: 30rem;
    }

    img.p-community-icon {
        height: 100%;
        /* https://codepen.io/sosuke/pen/Pjoqqp */
        filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(143deg) brightness(105%) contrast(104%);
    }

    a.p-community-icon {
        padding: 1rem;
        display: inline-block;
        height: 3rem;
        text-decoration: none;
        box-sizing: content-box;
    }

    a.p-community-icon:hover,
    a.p-community-icon:active {
        background: rgba(255, 255, 255, 0.11);
    }

    .zero-height {
        height: 0;
        position: relative;
        z-index: 1;
        top: -10rem;
    }

    .zero-height img {
        height: 5rem;
        position: relative;
        top: -0.25rem;
        margin-right: 1rem;
    }

    .zero-height .big-button {
        height: 3rem;
    }

    .big-button {
        box-sizing: content-box;
        display: inline-flex;
        align-items: center;
        text-decoration: none;
        line-height: 3rem;
        padding: 2rem;
        filter: brightness(100%);
        font-size: 1.75rem;
        backdrop-filter: blur(0);
    }

    .big-button:before {
        position: absolute;
        z-index: -1;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(0.5rem);

        clip-path: polygon(0 0, calc(100% - 1rem) 0, 100% 1rem, 100% 100%, 1rem 100%, 0 calc(100% - 1rem));
        content: "";
    }

    .big-button:hover,
    .big-button:active {
        filter: drop-shadow(0 0 1rem #f784f2);
    }

    .cross-platform > a > video {
        width: 24rem; 
    }

    @media (max-width: 700px) {
        .p-warning {
            margin-top: 0;
        }
        .p-logo {
            margin: auto;
            margin-top: 0;
            margin-bottom: -2rem;
        }
        .p-logo img {
            margin-top: -1rem;
        }
        .p-section {
            margin-top: 4rem;
            display: block;
        }
        .p-section h2 {
            text-align: center;
        }
        .p-section-right {
            margin-left: 0;
        }
        .p-section small {
            margin: 0;
            display: block;
            text-align: center;
        }
        .p-img-left {
            margin: auto;
            margin-top: 2rem;
            margin-bottom: -1rem;
            height: 6rem;
        }
        .p-img-right {
            margin: auto;
            margin-bottom: 2rem;
            margin-top: -1rem;
            height: 6rem;
        }

        .p-section.sponsors > div > div {
            text-align: center !important;
        }

        .p-section.sponsors > img {
            position: relative;
            left: -1rem;
            top: 3rem;
        }

        .p-early-stages-left {
            border: 0;
            padding: 0;
            height: auto;
        }

        .p-early-stages-left > p {
            font-size: 83%; /* <small> */
        }

        .p-section.get-involved > div {
            width: auto !important;
        }

        .p-section.get-involved > div > p {
            text-align: center;
        }

        .p-section.get-involved > div:nth-child(2) {
            margin: auto !important;
            margin-top: 2rem !important;
        }

        .p-section iframe {
            width: 100%;
            height: 15rem;
        }

        .choose-your-journey .content > video {
            width: 100% !important;
        }

        .community > .p-section > div {
            width: auto;
        }
    }


    @media (max-width: 1280px) {
        .choose-your-journey .options {
            flex-direction: column;
        }

        .choose-your-journey .engine,
        .choose-your-journey .core {
            clip-path: none !important;
        }

        .choose-your-journey .engine {
            background: linear-gradient(180deg, #06071b 0%, #56113d 50%, #06071b 100%) !important;
        }

        .choose-your-journey .core {
            background: linear-gradient(180deg, #06071b 0%, #263fb2 50%, #06071b 100%) !important;
            left: auto !important;
        }

        .choose-your-journey .content {
            width: 100%;
            text-align: center !important;
            padding: 1rem !important;
            align-items: center !important;
            align-self: center !important;
            left: auto !important;
            right: auto !important;
            margin-left: auto !important;
            margin-right: auto !important;
        }

        .zero-height {
            height: auto !important;
            top: 0 !important;
            margin: 0.5rem 0 2rem 0;
        }

        .cross-platform > a > video {
            width: 100%; 
        }
    }
</style>

<div class="choose-your-journey">
    <div class="options">
        <div class="engine">
            <div class="content">
                <h1>Mach <em>engine</em> <span style="font-size: 12px;">(coming soon)</span></h1>
                <h2>Composable, tooling-oriented, data-driven</h2>
                <span>Competitive in spirit with Godot/Unity/Unreal.</span>
                <span>Build games, GUI apps & more in the <a href="https://ziglang.org/">Zig programming language.</a></span>
                <video autoplay loop>
                    <source src="https://user-images.githubusercontent.com/3173176/164985604-8f86fac1-68aa-4f64-a33f-1f7f45219d31.mp4" type="video/mp4" />
                </video>
            </div>
        </div>
        <div class="core">
            <div class="content">
                <h1 align="center">Mach <em>core</em></h1>
                <h2>Window/Input/GPU, nothing else</h2>
                <span>Comparable to SDL/GLFW; but <em>truly</em> cross-platform.</span>
                <span>Desktop, Web (soon), and Mobile (future). Zig & C API.</span>
                <video autoplay loop>
                    <source src="https://user-images.githubusercontent.com/3173176/163732353-14657abc-d8d6-4367-847f-2b06821a1727.mp4" type="video/mp4" />
                </video>
            </div>
        </div>
    </div>
    <div class="zero-height">
        <a href="/docs" class="big-button">
            <img src="/img/wrench.svg" />
            Choose your journey
        </a>
    </div>
</div>

<div class="p-section built-with">
    <div style="text-align: left;">
        <h1 style="margin-top: 0;">Built with love, hard-work & Zig</h1>
        <img style="float: left; height: 5rem; margin-right: 1rem; margin-top: 0.5rem;" src="https://raw.githubusercontent.com/ziglang/logo/6446ba8e37a0651da720d8869e1ce9264fa0c0b9/zig-mark.svg" />
        <p><a href="https://ziglang.org">Zig</a> is a general-purpose simple programming language featuring compile-time code execution, blazing-fast compilation speeds, and bare-metal performance.</p>
    </div>
</div>

<div class="p-section p-section-highlight cross-platform">
    <a style="margin-right: 1rem;" href="https://user-images.githubusercontent.com/3173176/164985623-93e01957-a86b-4607-827d-2a6cda32a409.mp4">
        <video autoplay loop>
            <source src="https://user-images.githubusercontent.com/3173176/164985623-93e01957-a86b-4607-827d-2a6cda32a409.mp4" type="video/mp4" />
        </video>
    </a>
    <div class="p-section-right">
        <div style="text-align: left;">
            <h2>Cross-platform graphics in ~60 seconds</h2>
            <small style="margin-left: 1rem; display: inline-block; width: 35rem;">Just zig, git, and curl - no build tools, no system dependencies. (<a href="">how?</a>)</small>
        </div>
        <div>
            <code>
                <pre class="code">
git clone https://github.com/hexops/mach
cd mach/
zig build run-example-textured-cube</pre>
            </code>
            <small>
                Requires <a href="https://ziglang.org">zig 0.10.x</a> |
                <a href="https://github.com/hexops/mach/blob/main/doc/known-issues.md#known-issues">known issues</a>
            </small>
        </div>
    </div>
</div>

<div class="p-section">
    <div style="text-align: left;">
        <h2>Effortless cross-compilation</h2>
        <p>Windows, macOS, Linux & Steam Deck builds at the flip of a switch. WebAssembly, Android & iOS coming soon.</p>
        <code>
            <pre class="code">
<strong>$</strong> zig build -Dtarget=<strong>x86_64-windows</strong>
<strong>$</strong> zig build -Dtarget=<strong>x86_64-linux</strong>
<strong>$</strong> zig build -Dtarget=<strong>x86_64-macos</strong>.12
<strong>$</strong> zig build -Dtarget=<strong>aarch64-macos</strong>.12</pre>
        </code>
    </div>
</div>

<div class="community">
    <div class="p-section">
        <a href="https://twitter.com/slimsag">
            <img class="p-img-right" style="height: 20rem; margin-right: 2rem;" src="/img/wrench_rocket.svg" />
        </a>
        <div style="text-align: left">
            <h1>Community</h1>
            <small>Small but growing, you'll find most of us on Discord.</small>
            <br />
            <br />
            <a href="https://discord.gg/XNG3NZgCqp" class="p-community-icon">
                <img alt="Discord" class="p-community-icon" src="/img/discord.svg" />
            </a>
            <a href="https://github.com/hexops/mach" class="p-community-icon">
                <img alt="GitHub" class="p-community-icon" src="/img/github.svg" />
            </a>
            <a href="https://twitter.com/machengine" class="p-community-icon">
                <img alt="Twitter" class="p-community-icon" src="/img/twitter.svg" />
            </a>
            <a href="https://matrix.to/#/#hexops:matrix.org" class="p-community-icon">
                <img alt="Matrix" class="p-community-icon" src="/img/matrix.svg" />
            </a>
            <br />
            <br />
            <small><em>“One of the keys to a successful life in any field is learning to take responsibility for ourselves, rather than waiting for someone else to do something for us.” - Buzz</em></small>
        </div>
    </div>
    <div class="p-section">
        <div style="text-align: left;">
            <h2>Open source, always & forever</h2>
            <small style="margin-left: 1rem;">Apache or MIT licensed, at your choosing.</small>
            <p>
                Mach was created by Stephen Gutekanst, and <a href="https://devlog.hexops.com/2021/increasing-my-contribution-to-zig-to-200-a-month#i-grew-up-playing-linux-games-like-mania-drive">FOSS is in his roots.</a> We will always be
                beholden to our users and individuals, not investors.
            </p>
            <p>There's plenty to do, so if you're eager to get involved and contribute feel free to join the community!</p>
        </div>
        <a href="https://twitter.com/slimsag">
            <img class="p-img-left p-img-small" style="border-radius: 100%;" src="https://avatars.githubusercontent.com/u/3173176?v=4" />
        </a>
    </div>
    <div class="p-section sponsors">
        <div>
            <h2 style="text-align: center;">Sponsor development</h2>
            <p>Please consider <a href="https://github.com/sponsors/slimsag">sponsoring development</a>. It's not the amount that counts, but whether you believe in our vision. Special thanks to all these fine people for their support:</p>
            <div style="max-width: 50rem; text-align: left; margin-top: 1rem;">
                <!-- tier2 -->
                <a href="https://github.com/wilsonk"><img src="https://images.weserv.nl/?url=github.com/wilsonk.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/jamii"><img src="https://images.weserv.nl/?url=github.com/jamii.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/ziglang"><img src="https://images.weserv.nl/?url=github.com/ziglang.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/shintales"><img src="https://images.weserv.nl/?url=github.com/shintales.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/m3talsmith"><img src="https://images.weserv.nl/?url=github.com/m3talsmith.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/mitchellh"><img src="https://images.weserv.nl/?url=github.com/mitchellh.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/dzrw"><img src="https://images.weserv.nl/?url=github.com/dzrw.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/sid405"><img src="https://images.weserv.nl/?url=github.com/sid405.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/davidroman0O"><img src="https://images.weserv.nl/?url=github.com/davidroman0O.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <!-- tier2 -->
                <!-- tier1 -->
                <a href="https://github.com/mattnite"><img src="https://images.weserv.nl/?url=github.com/mattnite.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/andrewrk"><img src="https://images.weserv.nl/?url=github.com/andrewrk.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/Luukdegram"><img src="https://images.weserv.nl/?url=github.com/Luukdegram.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/Jack-Ji"><img src="https://images.weserv.nl/?url=github.com/Jack-Ji.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/kristoff-it"><img src="https://images.weserv.nl/?url=github.com/kristoff-it.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/tauoverpi"><img src="https://images.weserv.nl/?url=github.com/tauoverpi.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/TommiSinivuo"><img src="https://images.weserv.nl/?url=github.com/TommiSinivuo.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/jayschwa"><img src="https://images.weserv.nl/?url=github.com/jayschwa.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/jacobsandlund"><img src="https://images.weserv.nl/?url=github.com/jacobsandlund.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/jorangreef"><img src="https://images.weserv.nl/?url=github.com/jorangreef.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/karelp"><img src="https://images.weserv.nl/?url=github.com/karelp.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/ifreund"><img src="https://images.weserv.nl/?url=github.com/ifreund.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/shritesh"><img src="https://images.weserv.nl/?url=github.com/shritesh.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/user01"><img src="https://images.weserv.nl/?url=github.com/user01.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/silversquirl"><img src="https://images.weserv.nl/?url=github.com/silversquirl.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/teknico"><img src="https://images.weserv.nl/?url=github.com/teknico.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/LostKobrakai"><img src="https://images.weserv.nl/?url=github.com/LostKobrakai.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/jagt"><img src="https://images.weserv.nl/?url=github.com/jagt.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/ChrisGute"><img src="https://images.weserv.nl/?url=github.com/ChrisGute.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/dylanmcdiarmid"><img src="https://images.weserv.nl/?url=github.com/dylanmcdiarmid.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/MEATANDMEAT"><img src="https://images.weserv.nl/?url=github.com/MEATANDMEAT.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/johnburton"><img src="https://images.weserv.nl/?url=github.com/johnburton.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/ryupold"><img src="https://images.weserv.nl/?url=github.com/ryupold.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/genejo"><img src="https://images.weserv.nl/?url=github.com/genejo.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/hryx"><img src="https://images.weserv.nl/?url=github.com/hryx.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/r4gus"><img src="https://images.weserv.nl/?url=github.com/r4gus.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/batiati"><img src="https://images.weserv.nl/?url=github.com/batiati.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/kooparse"><img src="https://images.weserv.nl/?url=github.com/kooparse.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <a href="https://github.com/Manuzor"><img src="https://images.weserv.nl/?url=github.com/Manuzor.png?v=4&h=60&w=60&fit=cover&mask=circle&maxage=7d" width="60px" alt="" /></a>
                <!-- tier1 -->
            </div>
        </div>
    </div>
</div>
