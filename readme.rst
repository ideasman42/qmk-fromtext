QMK FromText (Ergodox)
======================

This is for anyone who'd rather keep their layout as a text file locally, avoiding online point-and-click utilities.

This is a single file utility that takes a keymap layout and writes out a ``hex`` file.
Use for creating keymaps locally (without compiling QMK).

Keymaps are an evaluated Python expression.

Run::

   qmk_fromtext my_keymap.py

This will write out ``my_keymap.hex``.

Both long and short identifiers can be used, to see available keys run::

   qmk_fromtext --list-keys

Example Keymap

.. code:: python

    (
        # Layer 1 (Qwerty)
        (
            # Left hand.
            GRV,   EXLM,  AT,    HASH,  DLR,   PERC,  LCBR,
            TAB,   Q,     W,     E,     R,     T,     LPRN,
            ESC,   A,     S,     D,     F,     G,
            LSFT,  Z,     X,     C,     V,     B,     LBRC,
            LCTL,  LGUI,  LALT,  MO1,   SPC,

                                               INS,   CAPS,
                                                      MO2,
                                        SPC,   ENT,   MO1,

            # Right hand.
            RCBR,  CIRC,  AMPR,  ASTR,  MINS,  EQL,   BSPC,
            RPRN,  Y,     U,     I,     O,     P,     BSLS,
                   H,     J,     K,     L,     SCLN,  QUOT,
            RBRC,  N,     M,     COMM,  DOT,   SLSH,  RSFT,
                          LEFT,  DOWN,  UP,    RIGHT, DEL,

            HOME,  END,
            PGUP,
            PGDN, ENT, SPC,
        ),
        # Layer 2 (KeyPad & FKeys)
        (
            # Left hand.
            ...,  F1, F2,  F3,  F4,  F5,  ...,
            ..., ..., ..., ..., ..., ..., ...,
            ..., ..., ..., ..., ..., ...,
            ..., ..., ..., ..., ..., ..., ...,
            ..., ..., ..., ..., ...,

                                     ..., ...,
                                          ...,
                                ..., ..., ...,

            # Right hand.
            ..., F6,  F7,     F8,   F9,     F10,  ...,
            ..., ..., KP_7,   KP_8, KP_9,   PSLS, F11,
                 ..., KP_4,   KP_5, KP_6,   PAST, F12,
            ..., ..., KP_1,   KP_2, KP_3,   PMNS, ...,
                      KP_0,   ...,  PDOT,   PPLS, ...,

            ..., ...,
            ...,
            ..., ..., ...,
        ),
    )
