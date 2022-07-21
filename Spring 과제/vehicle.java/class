import java.util.*;
public class Vehicle {
    protected final int num;
    protected String condition;
    protected int fuel = 100;
    protected int speed;
    protected int maxPassenger;
    protected int price;

    public Vehicle(int num) {
        this.num = num;
    }
    void getStatus(){
        System.out.println("번호: "+this.num);
        System.out.println("주유량: "+this.fuel);
        System.out.println("상태: "+this.condition);
    }
    //    운행 시작
    void startDrive() {
        if (this.fuel >= 10) {
            System.out.println("운행 준비 완료\n");
        } else {
            System.out.println("주유 해주세요\n");
        }
    }

    //    속도변경
    void changeSpeed(int inputSpeed) {
        if (this.fuel >= 10) {
            System.out.println("현재속력 : " + this.speed);
            System.out.println("변경할 속도 : " + inputSpeed);
            this.speed += inputSpeed;
            System.out.println("변경된 속도 : " + this.speed);
            System.out.println();
        } else {
            System.out.println("주유량을 확인해주세요.\n");
        }
    }

    //      상태변경
    public void changeCondition(String inputCondition) {
        if ("이용 불가능".equals(inputCondition) || "이용 가능".equals(inputCondition)) {
            this.condition = inputCondition;
        } else{
            this.condition = inputCondition;
            System.out.println("다시 입력해 주세요.");
        }
    }

    //      승객탑승

    void getPassenger(int a) {
        if ("이용 가능".equals(this.condition)) {
            if (this.maxPassenger - a > 0) {
                this.maxPassenger -= a;
                System.out.printf("탑승 승객 수: %d\n", a);
                System.out.printf("잔여 승객 수: %d\n", this.maxPassenger);
                System.out.printf("요금 : %d\n\n", a * price);
            } else {
                System.out.println("최대 승객 수 초과\n");
            }
        } else if ("이용 불가능".equals(this.condition)){
            this.condition = "이용 불가능";
            System.out.println(this.condition + "\n이용 불가능");

        }
    }



}
