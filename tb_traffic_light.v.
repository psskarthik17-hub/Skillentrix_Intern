module tb_traffic_light;

    reg clk;
    reg reset;

    wire red;
    wire yellow;
    wire green;

    traffic_light DUT (
        .clk(clk),
        .reset(reset),
        .red(red),
        .yellow(yellow),
        .green(green)
    );

    // Clock generations
    initial begin
        clk = 1'b0;
        forever #5 clk = ~clk;
    end

    // beging intial liness 
    initial begin
      $dumpfile("traffic.vcd");
      $dumpvars(0, tb_traffic_light);
      
        reset = 1'b1;
        #10;

        reset = 1'b0;
        #50;

        reset = 1'b1;
        #10;

        reset = 1'b0;
        #30;

        $finish;
    end

endmodule
