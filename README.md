# VIP

## Introduction
VIP (VHDL Interface Plug-in) is a script for VIM text editor which provides some facilities to copy paste entities, components and instances of components.

For example you can copy the component :

```
component mux is   -- place the cursor on this line and enter the command :Viy (Vhdl Interface Yank)
   port (
     INPUT  : in  std_logic_vector (15 downto 0);
     SEL    : in  std_logic;
     OUTPUT : out std_logic
   );
end component mux;
```

and paste it as an instance :

```
mux_0 : mux   -- place the cursor here and enter the command :Vii (Vhdl Interface Instance)
   port map (
      INPUT   => s_INPUT,
      SEL     => s_SEL,
      OUTPUT  => s_OUTPUT
  );
```

VIP can :

```
    copy an entity and paste it as
        an entity
        a component
        an instance
        a Verilog HDL instance

    copy a component and paste it as
        an entity
        a component
        an instance
        a Verilog HDL instance

    copy a instance and paste it as
        an instance (with auto-incrementation of the suffix number)
```

VIP tries to respect your indentation as much as possible (spaces, tabs, spaces + tabs).
