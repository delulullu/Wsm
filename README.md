* {

  box-sizing: border-box;

  padding: 0;

  margin: 0;

  user-select: none;

  -webkit-user-select: none;

}



p, h1, h2, h3, h4 {

  display: inline-block;

  margin-block-start: 0em;

  margin-block-end: 0em;

  margin-inline-start: 0px;

  margin-inline-end: 0px;

  padding-inline-start: 0px;

}



body {

  background-color: #9edae9;

  font-family: Arial, Helvetica, sans-serif;

  overscroll-behavior: contain;

}



.wrapper {

  position: fixed;

  top: 0;

  left: 0;

  width: 100%;

  height: 100%;

  pointer-events: none;

}



.bunny-radar {

  position: absolute;

  top: 0;

  left: 0;

  width: 100%;

  height: 100%;

  display: flex;

  justify-content: center;

  align-items: center;

  pointer-events: none;

}



.circle {

  position: relative;

  border-radius: 50%;

  z-index: 1;

  display: flex;

  justify-content: center;

  align-items: center;

}



.bunny-pos {

  position: absolute;

  width: var(--size);

  height: var(--size);

  border-radius: 50%;

  display: flex;

  justify-content: center;

}



.bunny-pos::after {

  position: absolute;

  content: '';

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAADhJREFUKFNjtFlz4j8DEYARpIYYxWCFxCiGKySkGEUhPsUYCnEpxqoQm2KcCtEV41WIrJigQphiAH0JGuGElBe4AAAAAElFTkSuQmCC);

  width: 20px;

  height: 20px;

  background-size: 20px;

  background-repeat: no-repeat;

  image-rendering: pixelated;

  bottom: -24px;

  transform: rotate(135deg);

}



.bunny-indicator {

  position: absolute;

  bottom: 0;

  color: #3cacc8;

  font-size: 0.8rem;

}



.end-message {

  position: fixed;

  height: 100%;

  width: 100%;

  display: flex;

  align-items: center;

  justify-content: center;

  flex-direction: column;

  z-index: 99999;

  animation: fade-in forwards 1s;

  pointer-events: all;

}



.end-message p {

  color: #57280f;

  background-color: #ffffff8b;

  width: 240px;

  padding: 30px;

  text-align: center;

  transform: translateY(calc(-100% - 10px));

}



button {

  font-family: Arial, Helvetica, sans-serif;

  border: 0;

  padding: 10px 20px;

  color: #4d220a;

  background-color: #c3ac83;

  cursor: pointer;

}



button:hover {

  background-color: #fff;

}



@keyframes fade-in {

  0% {

    opacity: 0;

  }

  100% {

    opacity: 1;

  }

}



.d-none {

  display: none;

}



.bunny {

  pointer-events: none;

}



.bunny::after {

  background-image: url(data:image/png;base64,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);

}



.sad .bunny::after {

  background-image: url(data:image/png;base64,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);

}



.happy-right .bunny::after,

.happy-left .bunny::after {

  background-position: 0;

  background-size: calc(var(--w) * var(--m)) calc(var(--h) * var(--m));

}



.happy-right::before,

.happy-left::before{

  position: absolute;

  top: -50px;

  left: calc(var(--m) * -0.5 * var(--h));

  width: calc(var(--m) * var(--h));

  content: attr(message);

  font-size: 0.8em;

  text-align: center;

  color: #57280f;

  animation: display forwards 0.8s;

}



@keyframes display {

  0% {

    transform: translateY(0);

  }

  90% {

    transform: translateY(-30px);

    opacity: 1;

  }

  100% {

    transform: translateY(-30px);

    opacity: 0;

  }

}



.happy-right .bunny::after {

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAgCAYAAAASYli2AAAAAXNSR0IArs4c6QAAAP5JREFUSEvdljESAiEMRaWz02PoabbUI2q5p9FjrJ0dTpjJTghsvhDGQhpmYfMIyScQdoNb6OFdTodIdvfnq7CvAi0Dmrs9luTH9XwsoAXQMpBzvDMNzYDIAM3TIn8A5OBTz8mQymiOIZLV74C1DCLvatJJWfbANNQNpBhysgI15KE00CHgOe4hUBugmEKgBrznORvaT1P2vQJpNMaYShJqDNUw1uN6lj2ZluKGxQF5vHlShnvoAcrqDXX4zZZJ2FlSPN5JrdKlVXhonYyat/S/vAGHAOV1mulwqypbcewusLVQNN/Lutbp5LmBXOp4oeaniGW4Fdeux5KVpOHADwr6DjBMkjHBAAAAAElFTkSuQmCC);

}



.happy-left .bunny::after {

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAgCAYAAAASYli2AAAAAXNSR0IArs4c6QAAAQNJREFUSEvdlj0OwjAMhcnGBseA03SEI8LY08AxYGMLctCr7NSxEyUw0KVS03x+/k3CZvATNN7psIv0/Xp/quuWhtUGgl1uj7TnfNyrUMugAHIYVORQz2ATsMbgHwCRHHojWTzLeYxdl70y/R1Qy6CnTiut5HIPLIcmYIwxtRrFQwt8jVLEcgECZkG9Nep9odBS4hlcKeSw1zwL9naaXK8FUEsKoDUwshbCx9ulsHsyzYv7e50yVGEPLJ/solOGFTYUDgOin0szr1SEXICoQ2xojeVwIJ/mOMPNc5mPptIUMie2NhuxoeYIFa3HA4+bAb+OdAFLWeWGuDH+f/NlyJtjw4FvuiQXMCR6vxcAAAAASUVORK5CYII=);

}



.hug-bunny-bear .bunny,

.hug-bear-bunny .bunny {

  --w: 32px;

  top: -42px;

}



.hug-bunny-bear .bunny::after,

.hug-bear-bunny .bunny::after {

  background-position: 0;

  background-size: calc(var(--w) * var(--m));

  image-rendering: pixelated;

}



.hug-bear-bunny .bunny::after {

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAAXNSR0IArs4c6QAAAZdJREFUWEfFl8FNBDEMRScHzuyBIqABWgEhrWgARDHQAJygFCqAHrhAAYjVX+kjj9eOE2dGO5edTTLxG9vfzpTpyFc5sv1pGODq/PQPL/H2+TPbyxvXLzwEACOvH9/7Pa8vNv8Q3rjl7TSANCI3BgihOC7hFvPAqgCMH2l1fDku18lQDHkAmz49P848dXd7byaZXIc1MDwcAgsANDAgLwtyVYCoXizmARjyvOBB0HgN0lOCKcNeAIZIJ58GsiAOADLGaSjyRAoAmzLh5L00innOnV1uZ0qQqkgBSAXozNcQ+A8Almb8yrCkAWQsI48QwErIRQAijwwDZGSIZ35PNtPDzfagEUUNye2GkRp0ZdTx1h3S6yfVdvz1/rI/bLRengxLKa6dtAd6qmLqPBCFQEqQ914l7AZoMc4ciMpvKglbAGTRsWp+SxHCmqFmZCnBU8Pq3bBWgFiaLSl2q8BrSN5pqGbcDYFXDXk21DlSOw2lASyIDEBNglUP1AA4x+xHbHlE7zmShwCWoagst35TcJ/0p1kE0jq/A+eTbjBgLTdgAAAAAElFTkSuQmCC);

  animation: hug-bear-bunny forwards 1.8s;

}



@keyframes hug-bear-bunny {

  0%, 4%, 95%, 100% {

    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAqJJREFUeF7tWstNRDEM3HfgDAeKgAZoBYSEaABEMdAAnKAUKoAeuEABCMTuM2IHecd2kvdL9rS7+byX8dgeJ+lWlX+6yte/mhwAp0f7X3+N8vT6UfQdi04eYVe1AMjCH1/et3A7Oz5Y/2ZMiAI3GQZUC4C2cHQfjQmpwI3OgAZAH/XR9xkDUoGT+WfLgAZAkDnIrMYARATzKbazfGydT+aJUjk6jjKgWgBk4Xf3tzsV7NXltUuZafPJPPIwlgWkn+gBb3+Nub8xoAHQR1XGALEEWhBpw+aR8VZLRgqrnzGslnAzoAEQNQWMmz0DUnGYHACyIGswjAIw1MJZLaHWAg0AZzaYOxP+1QKlGYBZpHQaZK4QToNRy+O4oWMC6oIGgDX6i6VQ4Wn/a5aW8TgOmWDV/Fo/9r/UBmYGVA+AJoGZ5mdMkPbDk4v1V6vlteDGqsvkGIBFUHUAaNE/1UWEAZpltRMjbxpNZkADgAiAqItoDMCdIObjTJ8UY0BqkBwdAKseYAhb2z/3Nqe+N+eb6O/1ZetzkEG4NzhaLTBZAIZiwlA1gHlPEClVuiqcPAACyNvzw9adHa/vsf4s+LHxrL3rup3Hf/RssFoA0AVSlZ5mqSgDWLUnWSVbDGgA9GeC7KzPWxx5GcCqRWwvzgBUgLMHgKW/3K6QiwFWZiQrwQaAEguse4PoMt4awBr9tX2FyTAgqgRHByC17E1lQHR/QMsG4WowuvGxGACYBmftURdg82rt2RkQfZFcDPA+3wxAdD9gqCyQa+Eyj1oNMkGEL1ItAHhvkAGn9Wd6gCk9r+9nY8BiAbDGgtIAYPDKdUeYMqAB0CPg9WkEDn1Tu7OrXdLG/pNnwOIAiC7Im6+9/XNd66e7wg0Ar2lm1t/MgJmty/y63yKelm4lf6/tAAAAAElFTkSuQmCC);

  }

  5%, 9%, 90%, 94% {

    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAplJREFUeF7tWttNAzEQzFUAHxQBDdAK/CAagGqgAfiCUqgAeuAHKgAJZaVk0GR2fbZzPjt/ie077+zsYxxPm84/U+f2bxYDwNX5yc+uM14/vqvsrcpLPCzrFgAz/OX9aw+n64vTv++KCXOBOzoDugWAGY7hwpgwFzh7z9EYMADYZn2MfcWAucDh85tjwAAgkTmsFA8GMGSwvuI8VZ9xvnoeywVYBaqFgNrwagEwwx+fHg52sHe396FOzfs8xQRVNWzT3k7yXw4YAGyzrPKYIW1MYHSJPsfrYSWwijNgAKBcEBw3JjXHgKCddPpiALAdepPhXAByG660hFsLDACC1aBVJlAtUIsBWE1yJUFvKCQ3QnM9ztaXygmsLxgAMNXGOjjzEI6z3/H5OI+tO7u8OUgy8yg7TfaeMocZ0D0ArAX29vy4nq1TDEDVZ9+VmkQZH2bAAECk/7khosoii31VlapVge4ByBUilgPMcyrGF8OA5gGorQZZn5CrJVYnQ4vRAir5KYqz8WQAajEBzxRred7sk/8MlVaFiwfg8+157+5OKhVZcszlcbavaZoOOlkyoHsAMASU6lPj6Clvz4+9v2KOSn7JOUAZqMZXD4BX7dk8xYDUTvBoDFgNAKr8eamu5jEGpKo+DDHFhOROUBnmZUKzAHgNVPLYe6anWt3oSZCsAioEBgDgEnZPQJ0uRxkQrQrFcgCTsfh7NwBENYL6Bwg9nXoiVI0BqwMg9TwgWh5VTx8FFjWDus4n1aC3GnirQqmTn2gDJMtglAF4b1ABp3JAVP0NAAABlfzcDPAyITcDSt8RHgBsEZBJMJUBuA5j1LIzu5SN2Tv3LfHiDFgdAF6DUuu2d13ua/zuEBgAeF3U2LwwAxqzT273F8R9am6Oncp/AAAAAElFTkSuQmCC);

  }

  10%, 89% {

    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAo5JREFUeF7tW0FOwzAQbA6c4cAj4AP9CggJ8QEQj6EfgBM8hRfAH7jAAxCINiu1I7az6ziO3WxviR3HOzs7u3bcbjHzXzdz+xcBQDBgYgQuzo5/tqfw8v61l5Xe/sy8yUPAa5C3f7UAiCHPb587c7w8P1lfIxO8/Znh0j4ZA7wGeftXC4BmiDZhYQQyBftrzGFAFGdAANCrPvOoeC4Y0IsiA2z0EMD0g7HF8jf218bTskIAAOmymAiKp1aPD3sF9fbm7t/8rXleG0/GEY9PrgEBQK/ajAHiafGgRhc2TrMMCABYyWVsb54BRjvVbtUBIDO1imEqAGh46jjegsi8FggAnNkg1YOlmVANAzCLsNKXAWwNBQrA2NTXDBnKhABA2VpDwAczQDyFFZ52HyeA/fD6dHm9fkRbE7D7bJUaADAxsWoArgFYzc+YIO3CANwhkmtNLItrwOwBYGqeqhHIAMZYZMroGsAmNFQkmwdAWyZbNSIA6NMgYxq2ZxPBUqtBec/30ebb4P3VJv97S2Kr4fI+WgcEAMAta13AsgKj9NiedzMgFxPYpikrcDTgvNRPBkAe/Hh92jnZwTzqbfeuBruuM4fz9lySHvobYLYADNWAsZhQLAQCgMx7g5ooHmwWwBBoBoBc1EeDvZ5mGuLVAnMWCAAyx753lSeeZYVS9QwQA2YPgLUkZh5PXQa7S+FcGqBtkDBxs4plMyGgGewNjWYZ0BwAqcth7xci7+kwmZeX+m4NCAB6BKxiiOcG2XOpR2OqZcDBAmANhVIApMZ+sgYEAEYt0M4Oa6fE5RsetrMCqBkGIHOwDmgOAKtBrMRl7bn/p4DvM+8HaBNllGYGsvbqAWAG1N4+mAG1G8jm9wsR+9xfCCflzgAAAABJRU5ErkJggg==);

  }

}



.hug-bunny-bear .bunny::after {

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAAXNSR0IArs4c6QAAAhRJREFUWEfdl71KA0EQx/cCki6ngqWNVc4XEB/EXLBIsLAJSiofRIxWFgkiJJcXER8gXiNYWIp6dkHIyhxOGDc7+3GLCKZJcruz89v/fOxeJP74E4X4bzVjCfZZXlRex2rIOUmbsRw/vJf8aRKLLP+wrqXbrNGIcwJQk2/nuGgr2RTT/M0bgjXQOWkn62KSFxEF+78Aul2aFMAxNc6wDj4D9dRxNgQ6ADAGR5h8dDFdDkAYL0cXy2kn3dMyhNTOG4ArWwCoiUU5jFumzuF5EMDnfC7W6nW2bQDA1ejc2FacATj5bU2rvRuLwXCgnaZzDhNXQlDVOXp9ub9hOZ0UCAGABB2QpFNJKgHQrNdVAD7Db1AAHCGI+ttaBVz9w2505aeWJoYAHMOHKlJJAVVGmyLBOSClXHYuLpsAglMkGKA8XslRays9Om5KQucyxAVtEKgCBeAqgHOu7QN0QZdwuCiwtddhW77XfcAlHLow9Lp99rISDEBDwYXAG8AWf6x9tc5NCnkloQsAOONKzrUJsUnoCqCrBE6VX1GASm5qQDDPCwAMdLdite8jgO0U9E5CWPhgZ0Nmj68/8oq7lCIAPfmo4VnaEcOn1buHtRGpuVAFwNQFrQCHSUPezorlZo73t8X13XPZO9TrNv5Xe0HvqC+mM/6NyfoqlSYNKWRU6jd2eAkFECmkAItFrWZ0blXApfWGzvkCkTGLMOCBzAMAAAAASUVORK5CYII=);

  animation: hug-bunny-bear forwards 1.8s;

}



@keyframes hug-bunny-bear {

  0%, 4%, 95%, 100% {

    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAp5JREFUeF7tW8tRAzEMJRXAhR6gAkqBEzQA1UADDBdohQagCA5QwTLDRAwRiPckyxvv2tzCyvbq6ekbZ3PQ+d+mc/0PqgNwfnI4/QT56fWj+pkeo1Z/mdUA4FVE5B9f3ncMcnF69PW5FSbQDOgWAK8lLXntl60wATKgWwCiloyu80TuTFmTAVFFousylfLsNQCw0IpaMrrOY7VM2WYYoNOsKOmtF6x9rP0GAKUuIOslr+vKz9pf5OX53f3tn6LXVzdU5SiWt/aRzfV+xQwYABRGJGECaznrOLS+OgOiOHQPgHYh1pJRwKvFgOgLNQcAW8iUKmx1h7UYYGWTX1mgWwD2pfhcLgAZMADYTm/ZSo6NAVaFqP/PpkP2XEvOzAK1GLB4AFgFkGV07W9Ni1FvoCs6nTXEwmxv8Z0F0OzPemHWZRYLgI7S8plVHDGjNAuIxb3MkTkDZMAAAJgwO0aI71q+jHwcMS49C3QPQKmLoPzv9fHZGbAaAESRWgXR3N2fPg/2AgMABdlcTHh7fkBuW/QcTZXTpsLRt2wWAFFomqadOz5RRa11tQE4Prv89woAvB/QLQA6BmQVPJoJUQawlWJaDBgAbG93WV2g97tBYYKXAagX0M+rM0BXgt42uTkAUP7PdoUsAFhm6PsG7u8FBgBGLIjGANQNWjV96SxQ9t07AxYHQGn7m9UVeucE6d0gmvKyJbOXAXosHh2Ghl2AVYyViwLA7q8BK84C3oORfHMAtD4YQfmenQSZLjAA2CKAKkKL2mw9oH8vgO756SiO5JHvV2PAagDwuoJlUdQ9SlRGFvUyAHWBkAEDAGcssH4D5L0Fzsp7GWPFLDgTZIPhagHQrmAh6b3Xjwok9jnLmDADBgCsKRYqB2PAQvWiX/sTefGybppczqgAAAAASUVORK5CYII=);

  }

  5%, 9%, 90%, 94% {

    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAppJREFUeF7tWstNBDEM3a0ALvQAFVAKnKABqAYaQFygFRqAIjhABYOE1tLuk7zv2TObyUzCDZJ44ufnL9luGv/ZNq7/phgAN5dnwz7Y71+/xb59zMjFLrEaAKKK2P63z58DQ9xenf//PjcTwgxoFoCoJb396I9zM0FmQLMAZC2ZPVc6LVMGZBXJnusAFEagM4ABnqVy9BzeI1ofYHpW5VXDAPXCnsFmB8AuZnkdKz/v4rb/+eXpYMvD/aNUKZrieB6/58mbjAEdABZMnHWPAbbdLOeJZ5ZHORhbJmdAFIfmAUDXUS0aBbpYDIherFoA1DyeVTiaFbLfYdnEjQHNAjCX4qdyhTADOgC76a1ayam+6VWI+HeWFtXvpSvBUzFg8QCoCjALmRzb502LvXrAfNrrHdg5Wgmy2Z93YdVlFgsARmnPgowBbF2NAdgjsApSrgRZDGAWZAqy9eoBYBXcVC4S9XEG7GQM6AAQqLMugtSP+vjsDBgbJKsBwBRhwZAhrq6rQU+Vp1aAtm/2brBaAEox4fvjNWvco+dYF0gZ0AHYITAMw8HbnqnNdSoG2D0vru+ODn7pVLh5ANRsEP2PkFlIZYDXBZocXC8eA5oHIFsIMQYwy1fDgNUBoPo+ywrMNTwGZC1fXSW4WgCYYmgJNlOM9v9RhngvTtK9QPMARINelAEY3ZFRbAaI5ydnQAfACf84EbJt3ti82nY4mwZXA0CpdlhlgBr1Vd+vZh6wWgDUNMkAwK5u7LtADF10HjA2FrD/GVYPQDQWmEKWdxmAUwOgzgHkGNAB2CHALImFEVZe3mNmZAr6qCcn+g7A61ppDBjLADzvKcgAQjnFAWCK2Hr0nT+bJ3jrKmBMvsyADgCDcqHrYQYsVE/32n9CbI5utjRgQAAAAABJRU5ErkJggg==);

  }

  10%, 89% {

    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAvNJREFUeF7tW71Ow0AMTiuhbvxJjCxMlBdAPAi0YgAxsCAQEw+CKEwMIIRE2xdBPAB0QWJgRPxtCIkgrjEiVoztS5rkeumWXi7Off782b4ktcDzX83z9QeFAbC2OBX+Bb83eCvkXgox+rPwsQFAu5BW5Pmru9dY9LWaU+a4N3jP1SmpjXkLgNaTAFQXeR6L8Fpz1vzVH7ykdo5E4K2NeAuA1JPt5rRxQDdSdwow5xhQARCpOBfLFQPGNQSksWzLADyPU3K4H3weaA83X50FKgCISo5CGjyKKz/qfGkdAGJ8fH6UeKndzb1YFqLsjYwBYNB7ALgYpOqAevAVG4q1jkEQUJ6HSaVhgHcAfH58mDVPNBratZvzQQNOzg+t5hfOgLEFQJr+Urntz+T20nB/oHPWUV1SGvtwUXEW8BaAvBeO3f10c6FiQOYaUAGgrPys3JUwCQqoDlHpcXakWsBqQFEMcAYAqtSVlsD4PHwMGgAexYzg/ue6wtQM8B4A3PTAsbT745omnAXA4zCP0ojcNQCY4C0AlCqnDRHn6wDnAQjDELfiXApOHLcNkcIZ4D0A4M68CyLbQkiq/uXvBqPnCtpSeGQAZMUErAWUoIx64WoGVAAgV2Uljlz9IGXC3PIGW9Yn2bKa9HMhbwGQPh63KhZS7AvsbO6b2do3S9QMqAAQvh8gZQCVFaSxD3acZYAzAGRVCeIFaz3NMWtkhVAFQMa7w9ouL+udIHUlmBUDwLD3AEh7Am7vD2tC6TWA2kTlxE0qls4AQC1YGxrOMsA5AOCGtaWw9gmRlOoYwNJWgmMHwOrCjNkl7t0//6tb2jdF8R4g9cyPMnrQ2jBDZw+676DU3aD3AEi3xvJigDbtYQapGVABECGw3pw0WnB5+5YYltsr8+b/0+vHGMjc2914nMsKO1vRTtCt3TdG1gzwHoDfUIiYEIRDLAHRq4y+BAVGhMHwEWUtsvBVr5vjvqXn1d0glX5avgPANTFlH7fWgLIvTHp/32FrFm4fo1/PAAAAAElFTkSuQmCC);

  }

}



/* hp bar */

.hug-bear-bunny::after,

.hug-bunny-bear::after {

  position: absolute;

  top: -55px;

  left: calc(-1 * var(--h));

  content: '';

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAGCAYAAACij5zfAAAAAXNSR0IArs4c6QAAADdJREFUOE9jZEAD4Rr8/9HFqMlfeeMjI7J5KByQ5egKqGk5yCx0O0YdMLhCABZH1I53ZPPQ0xgA1HAoB/krc8YAAAAASUVORK5CYII=);

  width: calc(var(--h) * var(--m));

  height: calc(6px * var(--m));

  background-size: calc(var(--h) * var(--m)) calc(6px * var(--m));

  background-repeat: no-repeat;

  image-rendering: pixelated;

}



.hug-bear-bunny::before,

.hug-bunny-bear::before {

  position: absolute;

  top: -55px;

  left: -24px;

  content: '';

  width: calc(24px * var(--m));

  height: calc(6px * var(--m));

  animation: top-up forwards 1.4s;

}



@keyframes top-up {

  0% {

    width: 0;

    background-color: #8a8a8a;

  }

  100% {

    width: calc(24px * var(--m));

    background-color: #36e9ce;

  }

}



.bear::after {

  background-image: url(data:image/png;base64,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);

}



.overflow-hidden {

  overflow: hidden;

}



.flex-center {

  display: flex;

  justify-content: center;

  align-items: center;

}



.sprite-container {

  position: absolute;

  --w: 20px;

  --h: 32px;

  --m: 2;

  width: 0;

  height: 0;

  z-index: 1;

}



.sprite-container:has(.bunny) {

  transition: 1s;

}



.sprite  {

  position: absolute;

  --x: 3; /* grid */

  --y: 4;

  top: calc(-1 * var(--w));

  left: calc(-1 * var(--w));

  --width: calc(var(--w) * var(--m));

  --height: calc(var(--h) * var(--m));

  width: var(--width);

  height: var(--width);

}



.sprite::after {

  position: absolute;

  bottom: 0;

  content: '';

  width: var(--width);

  height: var(--height);

  background-size: calc(var(--width) * var(--x)) calc(var(--height) * var(--y));

  background-repeat: no-repeat;

  image-rendering: pixelated;

  background-position: var(--bx) var(--by);

}



.map-cover {

  position: absolute;

  width: 100%;

  height: 100%;

  background-repeat: repeat;

  image-rendering: pixelated;

}



.map {

  position: absolute;

  top: 0;

  left: 0;

  transition: 0.4s;

  background-color: #b7e3ee;

}



.map.slow-transition {

  transition: 1.8s;

}



.map.transition {

  transition: 0s;

}



.player-wrapper {

  position: fixed;

  top: 0;

  left: 0;

  width: 100%;

  height: 100%;

}



.tree {

  position: absolute;

  width: 0;

  height: 0;

}



.tree > div {

  position: absolute;

  --w: 24px;

  --h: 30px;

  --m: 3;

  --width: calc(var(--w) * var(--m));

  --height: calc(var(--h) * var(--m));

  width: var(--width);

  height: var(--width);

  left: calc((var(--m) / -2) * var(--w));

  top: calc((var(--m) / -2) * var(--w));

}



.tree > div::after {

  position: absolute;

  content: '';

  bottom: 0;

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAeCAYAAAA2Lt7lAAAAAXNSR0IArs4c6QAAAKJJREFUSEvtlssRgCAMRKUwu7AdT7ZjFxamIzM4gIRdg8YLXIF9bD5M3ECubV32+Og4zY65Sh3KxYMwA4EASZyFVAFInIGIAFYcQYqAp+I1yA2gFZcgCaBVvAS5AG+J5xA7QNyVWjelxutJFv+7EC4fIm3M0W96QmwA+Uu0jnoVoZwm+3ZVpE0oa8d9DjBptJpd5BCNLv+OLUz4ugOf/5bZ9ACJXnYB/NLxRwAAAABJRU5ErkJggg==);

  image-rendering: pixelated;

  background-repeat: no-repeat;

  width: var(--width);

  height: var(--height);

  background-size: var(--width) var(--height); 

}



/* other */



.sign {

  position: fixed;

  font-family: Arial, Helvetica, sans-serif;

  color: #57280f;

  bottom: 10px;

  right: 10px;

  font-size: 10px;

  text-transform: none;

}



.indicator {

  position: absolute;

  top: 24px;

  right: 16px;

  color: #57280f;

  font-size: 16px;

  opacity: 0.8;

  z-index: 999;

  pointer-events: none;

  height: 32px;

  width: 36px;

  line-height: 40px;

}



.indicator::before {

  position: absolute;

  content: '';

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABIAAAAQCAYAAAAbBi9cAAAAAXNSR0IArs4c6QAAALRJREFUOE+llNsNgCAMRWUCHUMn0hF1Ih1DJ8CU2OZSofXBD5KWw6EIobna2LeRv6lftiPg2IunZEqa1x3nNdPQCcyL08QqiIIMK4EwLiC2YiW201ZWXOoQY8xqJLUbuqStt24alZKzwqkBGotRrQ6vQF8gvABbhT8QhN1AtIJXK51D4wz0BIIW+Ju4WyM4NcvyZqRPCA0t2wSq3TXr2DEmp4a33ytyyZhfieyp0HfOstLPzAmHG47SmZBqWwAAAABJRU5ErkJggg==);

  width: 36px;

  height: 32px;

  background-size: 100%;

  image-rendering: pixelated;

  left: -42px;

}



.indicator.happy::before {

  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABIAAAASCAYAAABWzo5XAAAAAXNSR0IArs4c6QAAAKNJREFUOE/lVMERgCAMsxPIGDqRjqgT6Rg6Qb1worVg68PzIz9oCGnSgyq1uqZmHI3zSrqG/V39AgZomJZ4v29DRmbVDyIJSkokmVf/K1FMqQ3RsnEPQSYpPTQ9KsX/DVEpWk+NHhHSJOg7DeUdmcZgfyFKAIushMmInrajcS6RVOapzDwqvYYzy7eoKH0NnsGW8fhy3h9IvMjMDJlPFjogOoVseByz1PgRF28AAAAASUVORK5CYII=);

  height: 36px;

  top: -4px;

}



a {

  color: #57280f;

  text-decoration: none;

  text-transform: none;

}



a:hover { text-decoration: underline; }



